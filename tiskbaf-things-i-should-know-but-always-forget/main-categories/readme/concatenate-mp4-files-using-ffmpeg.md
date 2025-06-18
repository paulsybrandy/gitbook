# Concatenate mp4 files using FFmpeg

Let’s start with the simplest use case which is to concatenate two mp4 files using FFmpeg. Let’s say you have two files file1.mp4 and file2.mp4.You can concatenate these files using the concat demuxer (documentation) easily if their properties match. That is, they have the same height, width, pixel formats, codecs, etc.There are two steps to using this command. First, you need to create a txt file with the names and paths of all the individual files that you want to concatenate. Then, you need to supply this list to FFmpeg as a commandline parameter.Let’s create the list first. Here is an example and let us call the list fileList.txt. In this example, both the files are in the home directory. each line starts with the keyword file and contains the path of the file within single quotes.

```
$ cat fileList.txt
file '/home/file1.mp4'
file '/home/file1.mp4'
```

Now, you can concatenate them using the following FFmpeg command`./ffmpeg -f concat -safe 0 -i fileList.txt -c copy mergedVideo.mp4`Here, you are using the concat command to read the list of video files that you created (fileList.txt) and copy the individual files in that order into an output file called mergedVideo.mp4. Remember, you are not re-encoding in this commandline because you are using the copy command.Concatenate all files in a directoryThis is a commonly asked question and it has to do more with shell scripting than actual FFmpeg usage. The first step you need to do here is to find all the mp4/avi/wav files in your directory and add them to a file. Then you can easily concatenate them as shown above.`for f in *.mp4 ; do echo file \\'$f\\' >> fileList.txt;`I ran this command in my video database folder and here is the output – looks good right?

```
file 'brooklynsfinest_clip_1080p.mp4'
file 'parkjoy_1080p50_crf1.mp4'
file 'riverbed_1080p25_crf1.mp4'
file 'simpsons_1080p2398_clip.mp4'
file 'simpsons_trailer.mp4'
file 'touchdown_pass_1080p.mp4'
file 'touchdown_pass_1080p_2997fps.mp4'
```

And, then you can concatenate them using the concat command we learned about earlier as follows.`./ffmpeg -f concat -safe 0 -i fileList.txt -c copy mergedVideo.mp4`
