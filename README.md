# X-Cart 4 Docker #

## Dependencies ##
[Docker](https://docker.github.io/engine/installation/)  

## How do I get set up? ##

1. Clone this repo.
2. Clone your X-Cart 4 repo inside here with the name "xcart" 
3. Download https://drive.google.com/file/d/1lJLPsfLAD5pCasw3vLHdnFEIIbtNVAOf/view?usp=sharing and put it in docker-entrypoint-initdb.d/ it should automatically be imported
4. Download https://drive.google.com/file/d/1TO_ZEa3KaBQK6CGtLsWU04n0SP9X8h5O/view?usp=sharing and put it in xcart/
you can do 5a and 5b at the same time
5a. Run `docker-compose up --build` (if you want this to run the in background use `docker-compose up --build -d`)
5b. Open a new terminal window, install node version 10 or 12 (you can use https://github.com/tj/n#installation) then go into xcart/ and run `npm install` and `gulp`

## How do I shut it down? ##

Run `docker-compose down` or close the terminal window
