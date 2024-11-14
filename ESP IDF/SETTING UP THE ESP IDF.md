- Go to the esp folder and run the command :
```
	export IDF_PATH=~/esp/esp-idf
	source $IDF_PATH/export.sh
```

- To set the target as esp 32 on the terminal :
```
	idf.py set-target esp32
```

- To set up esp idf :
```
	get_idf
```

- To build the files :
```
	idf.py build
```

- Now connect the esp 32 to the laptop via usb cable and then run the code :
```
	sudo chmod 777 /dev/cu.usbserial-0001
```

- Next run the code :
```
	Idf.py –p PORT [-b BAUD] flash
```

- To monitor the output given by the Wall-E on the laptop terminal :
```
	Idf.py –p PORT [-b BAUD] flash
```
