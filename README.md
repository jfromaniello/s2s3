Only for OS X.

Capture Screenshot and send it to Amazon S3.

## Install

Install with **npm** as follows:

~~~
npm i -g s2s3
~~~

Install with **brew** as follows:

~~~
brew tap jfromaniello/brew
brew install s2s3
~~~


Then you need to create a `~/.s2s3.config` file with something like this:

~~~javascript
{
	"ACCESS_KEY_ID":     "MY-ACCESS-KEY",
	"ACCESS_KEY_SECRET": "MY-KEY-SECRET",
	"REGION":            "MY-REGION", // e.g. eu-central-1
	"BUCKET":            "THE-BUCKET",
	"COPY_FORMAT":       "![{filekey}](http://THE-BUCKET.amazonaws.com/{filekey})",
	"PREVIEW_BEFORE_UPLOAD": true,
	"DIRECTORY":         "screenshots" //optional base key for the objets in s3.
}
~~~

ACCESS KEY, SECRET, REGION and BUCKET are the Amazon S3 parameters, COPY_FORMAT is a mask of what is going to by write to your clipboard after finished.

PREVIEW_BEFORE_UPLOAD (defaults to false) shows OSx preview application before uploading, this allows you to draw arrows and rectangles.

## Usage

From terminal:

~~~
$ s2s3
~~~

Grab the area of the screen you want to capture and you will get a link copied to your clipboard.

Create a global key shortcut to `/usr/local/bin/s2s3` as described here:

[apple.stackexchange.com: Create global shortcut to run command line applications](http://apple.stackexchange.com/questions/24063/create-global-shortcut-to-run-command-line-applications)

## License

MIT - 2013 - José F. Romaniello
