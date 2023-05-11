# Hyle-X
> Hide your personal Data inside The Audio wav file<br/>
> Written in C++ by Elkyw

Hyle-X is just Hyle but written in C++ . you may ask why c++ , idk just for fun..

**NOTE:** This tool only supports the `.mp3` and `.wav` audio files and can hide any other files inside the audio file.

## Version
**Hyle-X 1.2.1**

## Requirement
- [libboost-all-dev](https://packages.debian.org/search?keywords=libboost-all-dev)
    ```
    sudo apt install libboost-all-dev -y
    ```
- [cmake](https://cmake.org/)
    ```
    sudo apt install cmake -y
    ```

## Installation and Uses

### Automated Installation (Recommanded)
Change the directory to where you want to install this tool and run the follwing command
```
curl https://raw.githubusercontent.com/Elkyw/Hyle-X/main/install.sh -s | bash
```

### Manual Installation

- Make Sure all requirements are installed
```
sudo apt install libboost-all-dev cmake -y
```
- Git clone this repo and change the directory
```
git clone https://github.com/Elkyw/Hyle-X.git && cd Hyle-X
```
- Now Build the package
```
mkdir build && cd build && cmake ..
```
- Now make the final binary
```
make
```
- Copy the binary in `/usr/bin/` for easy access \(optional\)
```
sudo cp Hyle-X /usr/bin/
```

## How to Use

### Hiding Data
- For hiding files inside `.wav` audio file.
    ```
    ./Hyle-X -i input.wav -f filetobehidden.txt -o output.wav
    ```
- For hiding message inside `.wav` audio file.
    ```
    ./Hyle-X -i input.wav -m 'Dummy Message' -o output.wav
    ```

### Extracting Data

```
./Hyle-X -i output.wav
```
- If the hidden data is some message, it will be printed on the terminal.
- If the hidden data is a file, it will be extracted on the current directory.



