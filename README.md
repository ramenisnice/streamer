# Streamer

A live streaming application using ReactJS and Redux.

## Installation

1. Clone this repo
  
2. Install [Open Broadcaster Software](https://obsproject.com/) aka OBS for your operating system.


## Usage

### Backend - API Server

1. **Open New Terminal Window** & Please `cd` into `api` folder and then run `npm install`.

2. Run `npm start` to start this local server. This opens port `8001`.

3. Open [http://localhost:3005/streams](http://localhost:3005/streams) to view the fake api resource powered by `json-server`. The API Server is used for interacting with the Frontend.

### Backend - RTMP Server

1. **Open New Terminal Window** & Please `cd` into `rtmpserver` folder and then run `npm install`.

2. Run `npm start` to run RTMP Server on your local machine. This opens port `1935` for rtmp and port `8000` for http.

### Frontend - Client

1. **Open New Terminal Window** & Please `cd` into `client` folder and then run `npm install`.

2. Run `npm start` to run this on your local server. This opens port `3000`.

3. Login using the sign in button to view the streams created by you.

4. Open [http://localhost:3000](http://localhost:3000) to view the frontend part of the application within the browser.

## Streaming through OBS

1. Open OBS. For Live ScreenShare Recording, in the scenes sub window, click on "+" icon and create a new scene. After that on sources sub window, click on "+" icon multiple times and add "Audio Input Capture" & "Display Capture" respectively. For other types of streaming, consult Mr. Google!

2. Click on "Settings => Stream". Choose Streaming Type as custom streaming server. Set URL as `rtmp://localhost/live`.

3. For stream key, enter the stream id of the stream you want to play. For example, for URL `http://localhost:3000/streams/8` the stream id would be 8. Please insert that ID.

4. Click Ok and then start streaming. Stream should be available at `http://localhost:3000/streams/:id` where id is your stream id, which is the same URL to browse into for watching this stream.
