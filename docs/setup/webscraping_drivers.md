# Web Scraping Using an Automated Browser

Sometimes when we scrape the web, we need to automate our computer to open a web browser to gather information from each page.
This is especially true when the site we want to scrape has content that is loaded dynamically with javascript.

We will install one package to help us here: Chromedriver


Installing this stuff is operating-system specific, hence so are the instructions below.

## Mac Users

Make sure your `homebrew` package is up-to-date. To do so, open a terminal and enter

```
brew update
```

If that returns an error, `homebrew` is not installed.

- To install Homebrew, open a terminal and paste the following command:

	```bash
	ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
	```

- To verify that Homebrew installed correctly, enter the following into your terminal
	
	```bash
	brew doctor
	```

	...and you should see the following output
	
	```bash
	Your system is ready to brew
	```


### Chromedriver

* We assume you have Google Chrome installed. If not, do this first.

*   Install `chromedriver` via homebrew:
```
brew cask install chromedriver
```
*   Verify your install, by entering the following in your terminal. The expected output is `ChromeDriver 2.4X.X`
```
chromedriver --version
```


## Windows Users

### Chromedriver

*   Install Google Chrome from [here](https://www.google.com/chrome/browser/desktop/index.html)
*   Download the windows version of Chromedriver from [here](https://chromedriver.storage.googleapis.com/index.html?path=2.41/).
*   Extract the contents from the zip file, and extract them into a new directory under `C:\chromedriver`
*   Make sure that the chromedriver.exe file is directly under the PATH you specified, i.e. under C:\chromedriver. If your zip unpacker created a new folder with a different name inside your specified folder, move the .exe file to `C:\chromedriver`.
*   Add the directory `C:\chromedriver` to your PATH as described before.
*   If this went successfully, open a new Cygwin session, and enter `chromedriver --version`, you should get output that looks like `ChromeDriver 2.4X.XX`


## Linux Users

### Chromedriver

*   Open a terminal session
*   Install Google Chrome for Debian/Ubuntu by pasting the following and then pressing `Return`
```
sudo apt-get install libxss1 libappindicator1 libindicator7
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb

sudo dpkg -i google-chrome*.deb
sudo apt-get install -f
```
*   Install `xvfb` so chrome can run 'headless' by pasting the following and then pressing `Return`
```
sudo apt-get install xvfb
```
*   Install Chromedriver by pasting the following and then pressing `Return`:
```
sudo apt-get install unzip

wget -N https://chromedriver.storage.googleapis.com/2.41/chromedriver_linux64.zip
unzip chromedriver_linux64.zip
chmod +x chromedriver

sudo mv -f chromedriver /usr/local/share/chromedriver
sudo ln -s /usr/local/share/chromedriver /usr/local/bin/chromedriver
sudo ln -s /usr/local/share/chromedriver /usr/bin/chromedriver
```
*   Your install worked, you should get `ChromeDriver 2.4X.XX` returned if the installation was successful
```
chromedriver --version
```


!!! tip "Hat-tip"
    We borrowed quite liberally from Christopher Su to for instructions on [installing Chrome and Chromedriver](https://christopher.su/2015/selenium-chromedriver-ubuntu/).
