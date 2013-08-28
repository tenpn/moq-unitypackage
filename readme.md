A unitypackaged mirror of Moq

#Installation

Download latest unitypackage from https://github.com/tenpn/moq-unitypackage/releases

Drag into Unity3D editor window, add everything. Moq will now be available for editor-side tests. 

#Reference

The nuget version is available from here:

https://www.nuget.org/packages/moq

...cached to nuget-packages/.

Both this package and the Moq dlls are licensed under the BSD 2-clause license:
http://www.opensource.org/licenses/bsd-license.php

#Pull requests

There are no guarantees about how long after a Moq release this project is updated. If you want to send a pull request with an updated package, here's the build process:

- Move current nuget zip in nuget-packages/ into nuget-packages/previous
- Use NuTake (https://chrome.google.com/webstore/detail/nutake/ibhhbcaipjilldjkhhblhgdedjgoecap) or similar to download latest nuget package from https://www.nuget.org/packages/moq
- Commmit new nuget zip to nuget-packages/
- Update version number in Assets/Moq/readme.md 
- From zip, copy contents of lib/net35/ to Assets/Moq/Editor/ and commit all changes to git
- In Unity3D Editor, make a new unity package from the Assets->Export Package... menu
- Save that package to releases/
- Commit the new package with a tag of v[MoqVersionNumber]
- Push, send pull request.