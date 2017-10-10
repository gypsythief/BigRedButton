# Program: Big Red Button
# Home page: https://github.com/gypsythief/BigRedButton
# Author: Gypsythief
# Licence: MIT

************************************************************************

1) Intro

Big Red Button is a "safety button", a small and simple program to 
provide a floating button on the screen which, when clicked, will cover
the screen with an image. It is intended for use in Primary Schools to
allow pupils to easily hide the screen if they accidentally come across
something that makes them uncomfortable. They can then get their
teacher to deal with whatever it may be.

It was inspired by "Hector's World Safety Button", written by NetSafe
(https://www.netsafe.org.nz/) a New Zealand e-safety organisation.
Unfortunately, Hector's World was last updated for Windows Vista and no
longer runs on Windows 10; hence this replacement.

************************************************************************

2) Hacking

The software is publish under the MIT licence (see seperate licence
file for full details) which essentially says "here you go, have fun".
As a result the full source code is available from the website and you
are free to do virtually what you will with it.

All software used to create this program is free-as-in-speech and
free-as-in-beer, so if you do want to change things, it won't cost you
anything in licences.

The program was written in PWCT, so you will need this to edit the
source. PWCT is available at http://doublesvsoop.sourceforge.net
The file you will need to open is bigredbutton.ssf. The other files are
working files of PWCT, and are needed.

The graphics were created in Inkscape, available from
https://inkscape.org but should be editable in any vector graphics
program. The SVG files behind the graphics are in the "Resource Files"
folder on the website.

Graphics tweaks and file conversions were performed with GIMP, available
from http://www.gimp.org

The msi installer was created with Wix Toolset, available from
http://wixtoolset.org. The files for this are in the WixInstallerFiles
directory. Only wander in here if you have are truely masochistic. 

If you would like to simply change the graphics without getting
into editing the source, you can do this by simply replacing any of the
three image files bundled with the application. You will have to keep
the name, file type and size the same for each one:

BigRedButton.png : the main floating button. 70px by 70px

moveArrows.png : the little grab-handle icon. 20px by 20px

ScreenCover.jpg : the image that covers the screen. 1920px by 1080px

************************************************************************

3) The Release

There are two release files available.

i) The zip contains the program plus its associated graphics files.
This is fully portable, and will run without installation from anywhere.
A manual install might consist of dumping the extracted archive into
%PROGRAMFILES% and creating a link into the Startup directory of the
Start Menu. Uninstallation is just a case of deleting the files again.
If you don't trust MSI's you could easily push the files out onto
domain client computers using Group Policy Prefernces.

ii) The msi is intended for deployment via Group Policy onto a domain
netowrk. As such, it is non-interactive and just runs. It creates a
"Big Red Button" folder in %PROGRAMFILES% and copies the files into
that. It also creates a "Big Red Button" Start Menu entry with a link
to the program, and a Start Up shortcut. Being an MSI, it will also
generate any required registry entries. It registers to "Programs and
Features" for uninstallation.

If you don't trust MSI's you could easily install via method i) and push
the files out onto domain client computers using Group Policy
Preferences.
