# How to update node on mac

1.  Check node version

    > Type `node -v` in terminal
    >
    > > The output should read `x.x.x`

2.  Install/Check if `n` is installed

    > `sudo npm install -g n`

3.  Update your node to the desired version

    > 1.  install latest stable
    >     > `sudo n stable`
    > 2.  install latest
    >     > `sudo n latest`
    > 3.  install latest LTS
    >     > `sudo n lts`

4.  Verify new node version
    > `node -v`
    >
    > > readout should be `x.x.x`
