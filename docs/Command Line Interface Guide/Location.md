---
sidebar_position: 2
---

# Location

The location of the flirc_util command line application ships in different location on each operating system. The commandline application is installed alongside the GUI. Should a copy be presented by itself online, question it's authenticity.

## MacOS

The location of the commandline utiltity is embedded in the Flirc.app application.

`bash $ cd /Applications/Flirc.app/Contents/Resources/flirc_util`

The application is compiled statically so there is no additional resources or libraries needed to run flirc_util.

Rather than remembering the location of the commandline utility, it can easily be installed. This can be done with the following command:

`bash $ cp flirc_util /usr/local/bin/`

## Linux

The location of the commandline utiltity is installed side the Graphical User interface. The app is installed in /usr/local/bin which is in the $PATH. Running the application can be done by the following:

`bash $ flirc_util help`

## Windows

The location of the commandline utiltity is installed side the Graphical User interface and is installed in the C:\Program Files (x86)\Flirc directory. The application is uniquely named flirc_util.exe on windows. The application must be used and called from the windows command prompt.

```
C:\Users\user> cd "C:\Program Files (x86)\flirc"
C:\Program Files (x86)\flirc>flirc_util.exe help```

> Note - Remember to add the .exe extension when following the information or instructions in this guide. Not doing so will cause extremely confusing results.

