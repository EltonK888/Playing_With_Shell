# Playing With Shell
A few simple shell scripts used to organize images and create an html file.

**Important:** To use the scripts you must add `exiftime` to your PATH environment variable. `exiftime` is used to find information about the `.jpg` files.

To add `exifitime` to your PATH environment variable
```bash
$  export PATH=$PATH:/full/path/to/exiftime/bin
```

## Using the scripts

There are 3 shell scripts in the `src` directory

1. **`mkpics.sh`** - Takes in a column number and path to images and outputs to stdout an html file the images in a table with the number of columns. This can be redirected into an html file.

Example Usage:
```bash
$  ./mkpics 3 images/pics/pic1.jpg images/pics/pic2.jpg > mkpics.html
```

2. **`filepics.sh`** - Takes in a directory containing jpg images and creates directories that sorts the images by their year and then month.

Example Usage:
```bash
$  ./filepics.sh images/pics/
```

3. **`mkpics2.sh`** - Takes in a column number and the directory containing the folders created by `filepics.sh` and outputs to stdout an html file the images in a table with the number of columns. This can be redirected into an html file.

Example Usage (after `filepics.sh` creates the directories):
```bash
$  ./mkpics2 3 . > mkpics2.html
```

This will create an html file that is similar to the following image
![example html](https://github.com/EltonK888/Playing_With_Shell/blob/master/example.JPG)
