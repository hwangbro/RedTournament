# Restream PC setup
- Instructions for if you want to setup your own system to run restream
- This makes a lot of assumptions about prior knowledge and is not comprehensive. It assumes some familiarity with the command line and git

## Download zip
- dm me on discord if you dont have link

## Install the font in the zip

## Install some music player
- I personally use https://www.foobar2000.org/

## Install vb audio cables
- This is mostly used for the commentary feed (screen share) to have game audio

## Install node
- System worked with node v20.19.5, YMMV with anything else

## NodeCG setup
- Clone https://github.com/nodecg/nodecg, checkout tag v2.2.1
- Inside the bundles/ folder inside newly cloned nodecg, clone these two repos
    - https://github.com/pokemonSpeedruns/nodecg-speedcontrol, checkout branch v2.5.0-patch
    - https://github.com/hwangbro/red-24-layouts
- Create a new folder inside the top level of nodecg named `cfg`
- Copy bundles/red-24-layouts/config/nodecg-speedcontrol.json into the cfg folder.
- In the top level nodecg folder, run `npm install` and `npm run build`
- Inside nodecg-speedcontrol, run `npm install`
- On the top level, running `npm start` should launch nodecg. Running this in the future will require running `npm start`
- You should now be able to access local nodecg via `localhost:9090` in your browser

## OBS setup
- Click through the scenes and make sure the layouts are loading properly with local nodecg
- If it isn't set, go to Settings -> Audio, ensure `Monitoring Device` is set to `Cable Input (VB-Audio Virtual Cable)`
- If you click any of the audio tracks in the audio mixer -> `Advanced Audio Properties`, make sure that all audio sources that you would want to be audible to the commentators is set to `Monitor and Output`
- I would advise against juggling stream keys manually. Using the different profiles will have their respective stream keys already entered.
