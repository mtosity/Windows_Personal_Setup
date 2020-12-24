# Windows_Personal_Setup

My personal setup for a fresh windows

[Windows 10 LTSC 2019](https://drive.google.com/file/d/11-Uz-W0g0aL_4v5Rv6MuR6ykvaDH3COr/view?usp=sharing)

## Download Links:

* Basics:

[Chrome](https://www.google.com/chrome/)

[VLC](https://get.videolan.org/)

[RAR](https://www.rarlab.com/download.htm)

[Adobe PDF](https://get.adobe.com/reader/)


* Editing:

[OBS Studio (Stream + Video Recorder)](https://obsproject.com/)

[HitFilm Express (Video Editing)](https://fxhome.com/hitfilm-express)

[Figma (Design)](https://www.figma.com/)


* Development:

[Visual Studio Code](https://code.visualstudio.com/)

[Visual Studio Community](https://visualstudio.microsoft.com/downloads/)

[Git](https://git-scm.com/downloads)

[Java](https://www.java.com/en/)

[Android Studio](https://developer.android.com/studio)


* Games

[Garena](https://www.garena.vn/gpc)
[League Of Legends (Sync to gg drive every update, Garena VN server)](https://drive.google.com/drive/folders/1ePfpqvSlo3wHA-dQFbCgGX7aroM3yLme?usp=sharing)

## Cloning all repos 

CNTX={users|orgs}; NAME={username|orgname}; PAGE=1
curl "https://api.github.com/$CNTX/$NAME/repos?page=$PAGE&per_page=100" |
  grep -e 'git_url*' |
  cut -d \" -f 4 |
  xargs -L1 git clone
