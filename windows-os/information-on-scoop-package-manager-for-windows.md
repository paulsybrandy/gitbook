# Information on ‘scoop’ package manager for Windows

### **What are buckets?**

In Scoop, buckets are collections of apps. Or, to be more specific, a bucket is a Git repository containing JSON [app manifests](https://github.com/ScoopInstaller/Scoop/wiki/App-Manifests) which describe how to install an app.

### Main ‘scoop’ command

By default, when you run `scoop install <app>`, it looks in the main bucket, but it's possible to install from other buckets too.

### **Known buckets**

There is a list of known buckets by the community, those can be seen in [`buckets.json`](https://github.com/lukesampson/scoop/blob/master/buckets.json), to see the list of known buckets execute:

```
scoop bucket known
```

### **Installing from other buckets**

If you want to install from a bucket besides the main one, you need to configure Scoop to know about the bucket. For example, to add the optional 'extras' bucket, run:

```
scoop bucket add extras
```

The 'extras' bucket is a [special bucket](https://github.com/lukesampson/scoop/blob/master/buckets.json), in that it's "well known", i.e. Scoop already knows where this bucket is so you don't have to specify its location.Just say the extras bucket wasn't well known, the way you'd add it would be:

```
scoop bucket add extras https://github.com/lukesampson/scoop-extras.git
```

That is,

```
scoop bucket add <name-of-bucket> <location-of-git-repo>
```

You can run `scoop help bucket` for more information on buckets.
