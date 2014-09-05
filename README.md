S3
==

A plugin that allows for S3 to be the media storage for the platform.

First and foremost:  If at any point you have questions, comments or concerns you can find us hanging out on 
twitter [@getpencilblue](https://twitter.com/GetPencilBlue) and on our 
[Sub-Reddit](http://www.reddit.com/domain/pencilblue.org/).  We're always happy to help and pull requests (plugin 
or core) are always welcome. 

Installation:
1) Clone repo into your PencilBlue's **plugins** directory.
2) Edit your config.json file to configure the media provider
```
{
  "media": {
    "provider": "/plugins/s3/include/s3_media_provider.js",
    "bucket": "S3_BUCKET_NAME_HERE"
  }
}
```
3) Start or restart your PB instance
4) Navigate to **Manage Plugins** section in PencilBlue
5) Install the **s3** plugin
6) Upon successful install click the **Settings** button for the s3 plugin
7) Enter your S3 Access Key and Secret Access Key
8) Optionally, enter your region.
9) Click Save

You should be good to go!

**NOTE:**
Currently there is no way to migrate data from one media provider to the other.  If "uploaded" media already exists 
that was created from a different provider then you must delete it and upload it.  You will also have to re-link any 
system objects that rely on that media until you can replace the content for a media object.  See 
https://github.com/pencilblue/pencilblue/issues/218
