# How to install oh-my-posh temes on Ubuntu20.04 

Open https://ohmyposh.dev/docs/installation/linux and then check the command lines.

To download Oh my Posh:
``` 
sudo wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/posh-linux-amd64 -O /usr/local/bin/oh-my-posh
sudo chmod +x /usr/local/bin/oh-my-posh
``` 

Donwload Oh My Posh Themes:

``` 
mkdir ~/.poshthemes
wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/themes.zip -O ~/.poshthemes/themes.zip
unzip ~/.poshthemes/themes.zip -d ~/.poshthemes
chmod u+rw ~/.poshthemes/*.omp.*
rm ~/.poshthemes/themes.zip
```

This will create a folder in your home directory.  To access this folder, just type ``` cd ~/.poshthemes ``` to check its themes. You can also visit the official website:  https://ohmyposh.dev/docs/themes

To configure your theme, you'll have to open the profile config. For this, I'm using vim, but feel free to use the editor you want:

``` vim ~/.profile ``` 

In the end of the file, simply add the line to configure the theme you chose:

``` eval "$(oh-my-posh --init --shell bash --config ~/.poshthemes/capr4n.omp.json)" ```

In this example, im using **capr4n** theme, but you can change inserting its name here, for example:

```eval "$(oh-my-posh --init --shell bash --config ~/.poshthemes/{theme}.omp.json)" ```

To change how the theme look, you can change the .json file.

To open it, just go to ``` cd ~/.poshthemes/```, open the file and edit its configs, colors, etc.

Tip: You can clone my repository on your machine and add the file ``` HeitorPupim.omp.json```to your theme folder and appy it. It will look like this:

![image](https://user-images.githubusercontent.com/50893051/184648735-5ac797d8-9051-4bb7-8ba0-ba1c26e12817.png)


