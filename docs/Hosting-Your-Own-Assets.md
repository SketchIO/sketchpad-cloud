# Hosting Your Own Assets

You have the option of using your own assets by providing a media URL when configuring your instance. This media URL needs to be a basic web server which returns the actual media files and the JSON config files. Simply upload the example `media/` directory to a publicly accessible URL and you’re set. This document provides a few examples of where you can host your files.

## AWS S3 Bucket
1. Create an S3 bucket in AWS
2. Upload the media directory in it’s entirety to the S3 bucket.
3. Ensure the uploaded resources are publicly accessible.

## Static Web Server
1. Upload the media directory to a static file server and ensure the uploaded resources are publicly accessible.

---

# Configuring Clipart
Your own clipart can be added to your instance by serving a Clipart.json file from your media server. Clipart.json is an array of Clipart objects which need a `key`, `title`, `type`, `value`, `preview`, `width`, and `height`. Follow the example Clipart.json in the media directory to build out your assets.

## JSON

```json
[
    {
        "key": "9357a236b87105b27847b0ff336f0299",
        "title": "Stone Giant",
        "type": "clipart",
        "value": "clipart/animals/stone-giant.svg",
        "preview": {
            "url": "thumb/clipart/animals/stone-giant.png",
            "width": 80,
            "height": 80
        },
        "tags": [
            "animals"
        ],
        "width": 210,
        "height": 219
    }
]
```

## File Formats
Clipart are best served as SVG in Sketchpad with a PNG preview. However, Sketchpad supports many raster image file types for clipart such as JPG and PNG.