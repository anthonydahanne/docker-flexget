Flexget Docker
==============

[FlexGet](http://flexget.com/) is a multipurpose automation tool for content like torrents, nzbs, podcasts, comics, series, movies, etc.

From this Docker image, you'll be able to create containers with flexget and the [cfscraper plugin](https://gist.github.com/cvium/8a585b544a98a36434a6) (that itself needs the [cloudflare-scrape module](https://github.com/Anorov/cloudflare-scrape) that itself needs a JS runtime, I used nodejs) and the transmission plugin.

I provied a sample configuration config.yml.sample, feel free to adapt ([use the documentation](http://flexget.com/wiki/Configuration)) and copy to config.yml in your current folder and then run :

    docker run -v $PWD:/usr/src/app --name flexget -d flexget

To check everything is fine, have a look at the logs :

    docker logs -f flexget

Or get a shell into the container and try out things :

    docker exec -it flexget bash
    # flexget -h
