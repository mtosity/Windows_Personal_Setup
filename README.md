# Windows_Personal_Setup

My personal setup for a fresh windows

[Windows 10 LTSC 2019](https://drive.google.com/file/d/11-Uz-W0g0aL_4v5Rv6MuR6ykvaDH3COr/view?usp=sharing)

## Download Links:

### Basics:

[Chrome](https://www.google.com/chrome/)

[VLC](https://get.videolan.org/)

[RAR](https://www.rarlab.com/download.htm)

[Adobe PDF](https://get.adobe.com/reader/)


### Editing:

[OBS Studio (Stream + Video Recorder)](https://obsproject.com/)

[HitFilm Express (Video Editing)](https://fxhome.com/hitfilm-express)

[Figma (Design)](https://www.figma.com/)


### Development:

[WSL](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

[Visual Studio Code](https://code.visualstudio.com/)

[Visual Studio Community](https://visualstudio.microsoft.com/downloads/)

[Git](https://git-scm.com/downloads)

[Java](https://www.java.com/en/)

[MinGW CPP](https://osdn.net/projects/mingw/releases/)

[Android Studio](https://developer.android.com/studio)

[Docker](https://www.docker.com/get-started)

### Games

[Garena](https://www.garena.vn/gpc)

[League Of Legends (Sync to gg drive every update, Garena VN server)](https://drive.google.com/drive/folders/1ePfpqvSlo3wHA-dQFbCgGX7aroM3yLme?usp=sharing)

## Docker for DB

### Mongodb

```
docker pull mongo
docker run -d -p 27017:27017 --name mongodb mongo
```

Connect via [Mongo Compass](https://www.mongodb.com/try/download/tools)

### Postgres

```
docker pull postgres
docker run --name postgres -e POSTGRES_PASSWORD=1212 -e POSTGRES_USER=user -p 5432:5432 -d postgres
```

Connect via [dbvis](https://www.dbvis.com/download/11.0)

If you use pgAdmin 4 to connect Postgres:

```
docker pull dpage/pgadmin4
docker run --name pgadmin4 -p 80:80 -e 'PGADMIN_DEFAULT_EMAIL=mtosity@gmail.com' -e 'PGADMIN_DEFAULT_PASSWORD=1212' -d dpage/pgadmin4
```

And go to localhost:80 log in to pgAdmin

Create new server with the info:

- username: user
- password: 1212
- host: 172.17.0.3

Host ip is the ip of the Postgres docker, to check it run `docker inspect postgres` and find IPAddress

## Cloning all personal repos

CNTX={users|orgs}; NAME={username|orgname}; PAGE=1
curl "https://api.github.com/$CNTX/$NAME/repos?page=$PAGE&per_page=100" |
  grep -e 'git_url*' |
  cut -d \" -f 4 |
  xargs -L1 git clone
