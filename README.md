## Pixelbook Programming

This project documents how I use pixel book for programming. Some issues I faced and fixed.
Make sure your pixelbook is linux enabled.

### Anaconda with ipython notebook enabled
Setup a env for python 3 and make sure the notebook is run in 0.0.0.0
```
source ~/anaconda3/bin/activate cartoenv
cd ~/
jupyter notebook --ip=0.0.0.0
http://penguin.linux.test:8888
sudo -u postgres psql postgres
```

### Atom.io 
Download and install atom editor, you may install from deb directly.
```
sudo apt-get install ./atom-amd64.deb
```
Change the font-size of the atom
```
// add to .atom/style.css
@font-size: 14px;
html, body, .tree-view, .tab-bar .tab {
  font-size: @font-size;
}
```
Install common atom packages
```
packages
atom-beautify
emmet
fileicons
minimap
pigments
```
Hide the hidden files
```
'tree-view':
    'hideIgnoredNames': true

1- From the Menu Bar go to File > Settings > Packages type in the Filter "tree-view" click on the setting of this package and then check the "Hide Ignored Names" choice.
2- Now go to "Core Setting" by File > Settings . In the Ignored Names box enter .* this will Hide ALL the hidden files/folders .
```



### Apt-Get commands
Add / Update / Deleete
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install <file>
sudo apt-get autoremove
```
Where is the packages repositity link located
```
/etc/apt
```

Install NodeJS
```
sudo apt-get install gnupg
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs
```


### Services Start/Stop
```
sudo /bin/systemctl daemon-reload
sudo /bin/systemctl enable elasticsearch.service
sudo systemctl start elasticsearch.service
```

### Curl
```
curl -s -X POST http://localhost:9200/
curl -s -X DELETE http://localhost:9200/
```
