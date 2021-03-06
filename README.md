#gmusicapi: an unofficial Python API for Google Music

The project is not supported nor endorsed by Google. I'll be interning for Google this summer, so to avoid conflicts of interest I'll stop contributing sometime in May. Get in touch if you're interested in taking over maintenance.

**Respect Google in your use of the API**. Use common sense (protocol compliance, reasonable load, etc) and don't ruin the fun for everyone else.

Official documentation is provided by Read the Docs: [documentation](http://readthedocs.org/docs/unofficial-google-music-api/en/latest).

Feel free to email me or - better yet - open an issue for bugs, feature requests, or contributions.

##Features

Implemented in version 2012.03.04:

* Getting library information:
    * all song metadata
    * all user playlist (auto, instant mix, and user-defined) titles and ids
    * songs from a specific playlist

* Song streaming and downloading

* Song uploading (only mp3s supported, currently)

* Playlist manipulation:
    * creation
    * name modification
    * song addition and removal
    * deletion

* Song manipulation:
    * metadata modification (be sure to read protocol_info)
    * removal from library

* Searching for songs, artists, and albums.

What's on the way:

* integration with the Android service api
* better packaging

##Usage

gmusicapi.api.Api is the user-facing interface.
To get started, install the dependencies and see example.py. For more information, see the [documentation](http://readthedocs.org/docs/unofficial-google-music-api/en/latest) and testing code.

##Dependencies

The API has been tested on Python 2.7.2 on Linux.

Currently, the following third party modules are used:

* [decorator](http://pypi.python.org/pypi/decorator)

* [mutagen](http://code.google.com/p/mutagen)

* [protobuf](http://code.google.com/p/protobuf)

* [mechanize](http://wwwsearch.sourceforge.net/mechanize/)

* [validictory](http://pypi.python.org/pypi/validictory) 0.8.1+

The first four are in Ubuntu's repos:
    
    python-decorator python-mutagen python-protobuf python-mechanize

You probably want to use easy_install to get validictory.


##Ports and Forks

I've seen a lot of excitement about possible ports, especially for mobile and web use. If you want to, go for it! 

You'll probably want to ignore anything related to Music Manager, since that's just for uploading. Information on uploading is [here](https://github.com/simon-weber/google-music-protocol).

Keep in mind that ports are likely to be considered derivative works under the GPL, and, again, be sure to respect Google.

Lastly, get in touch if you're working on a port. I might be able to help out.

##Notes

This is a work in progress, so debug logging is enabled by default.
All logging is done to gmusicapi.log in your working directory, and warnings and above are printed to the console.
Nothing authentication-related gets logged aside from "logged in" and "logged out" messages.


- - -
  

Copyright 2012 [Simon Weber](https://plus.google.com/103350848301234480355).  
Licensed under the [GPLv3](http://www.gnu.org/licenses/gpl.txt).
