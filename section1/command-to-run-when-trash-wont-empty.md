# Command to Run when Trash Won’t Empty

`sudo chown -cR $(id -un):$(id -gn) ~/.local/share/Trash/@(files|info)/*`
