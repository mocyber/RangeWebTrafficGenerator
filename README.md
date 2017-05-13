[![Build status](https://ci.appveyor.com/api/projects/status/yuyfcrhjgvvc9og9/branch/master?svg=true)](https://ci.appveyor.com/project/theturingnerd/walktheinterwebs/branch/master)


# HTTP/HTTPS Traffic Generation - Range Tool

This tool will allow you to install a service which generates very realistic browsing traffic for a range. We use this tool to generate cover traffic and simulate a user's browsing behavior.

This repository will contain the release compiled code only. You can find the original source for the repo at https://git.innov8tive.io/Innov8tive/WalkTheInterwebs. Internally, we refer to this tool as "WalkTheInterwebs". The reason for this will be apparent when you see the tool in action.

The tool functions by downloading a list of sites from a text file configured in the application settings. Typically, the site hosting the text file with sitelists is accessed via a secondary (hidden) private network. This allows a control plane to exist outside of range traffic and prevents giving away the site list being utilized in the traffic plane.

We use vagrant to compose linked clones on vsphere which run this service. We'll be releasing all of the vagrant files and shell scripts necessary to compose the entire environment soon. Please keep checking back.

In the meantime, you can install this service by grabbing the compiled artifacts from this repo and placing them into a directory. From an administrative command prompt, simply type `WalkTheInterWebs.exe install`. That will install the windows service. The windows service can run as local system, and should be allowed to interact with the desktop. If you forget to allow interaction it will still function but you cannot observe the behavior.

A future version of this product takes advantage of various browsers. This version is our early v1.0 release and only uses chrome. Please make sure chrome is installed to leverage this tool.

If you have any issues, questions, or comments feel free to contact me on twitter, or file an issue. @turingnerd.
