# Youtube Comments to Images

1. Save a youtube html page with comments
2. Run the `convert.py` python script to generate the png files containing the comments
```shell
$ python convert.py commnets.html
```
3. The output is in the `out` directory

# Basic functionality

- The script will create a an `out` directory to output the images to.
- The script generates an `index.html` file to save the progress and uses [Html2Image](https://pypi.org/project/html2image/) to convert that file to an png.
- `youtubestrap.html` contains the styles found in the head of any youtube video web page and the body that will be used to wrap a single comment.
- `comments.html` is an example file with the comments from the [Sigma Male Theme Song](https://www.youtube.com/watch?v=1-emQo-7O3Y) video - engineer grindset.
- The script looks for the `ytd-comment-renderer` tag in the html file so its ok if the input file does not contain the entire web page and only a few copy pasted comments with inspect element.
- The `div` tag in the `youtubestrap.html` file with the id `HEREISCONTENT` will wrap the comment with the tag `ytd-comment-renderer` so don't remove that or change it.
