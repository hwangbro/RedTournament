# Restream PC setup
- Instructions for if you want to setup your own system to run restream

## Download zip
- link to zip

## Install the font

## Install some music player
- I personally use https://www.foobar2000.org/

## Install vb audio cables
- This is mostly used for the commentary feed (screen share) to have game audio

## Install node
- Ran with node v20.19.5

## NodeCG setup
- Clone https://github.com/nodecg/nodecg, checkout tag v2.2.1
- Inside the bundles/ folder inside newly cloned nodecg, clone these two repos
    - https://github.com/pokemonSpeedruns/nodecg-speedcontrol, checkout branch v2.5.0-patch
    - https://github.com/hwangbro/red-24-layouts
- Create a new folder inside the top level of nodecg named `cfg`
- Copy bundles/nodecg-speedcontrol/config/nodecg-speedcontrol.json into the cfg folder.
- In the top level nodecg folder, run `npm install` and `npm run build`
- Inside nodecg-speedcontrol, run `npm install`
- On the top level, running `npm start` should launch nodecg. Running this in the future will require running `npm start`

## OBS setup
