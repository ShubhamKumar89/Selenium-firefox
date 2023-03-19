# Selenium-firefox


[Selenium](https://pypi.org/project/selenium/) is an open-source tool that automates web browsers. It provides a single interface that lets you write test scripts in programming languages like Ruby, Java, NodeJS, PHP, Perl, Python, and C#, among others.

## Dependencies

```
sudo apt update
sudo apt install -y python3-pip
```

### Verify

```
$ python3 --version

Python 3.10.6
```

## Install Browser

```
sudo apt-get install firefox
```

### Verify

```
$ firefox --version

Mozilla Firefox 111.0
```

## Install WebDriver

Selenium requires a [driver](https://github.com/mozilla/geckodriver/releases) to interface with the firefox browser. `Firefox`, for example, requires `geckodriver`, which needs to be installed before the below examples can be run.

```
sudo apt-get install firefox-geckodriver
```

### Verify

```
$ geckodriver --version

geckodriver 0.32.2 ( 2023-03-10)

The source code of this program is available from
testing/geckodriver in https://hg.mozilla.org/mozilla-central.

This program is subject to the terms of the Mozilla Public License 2.0.
You can obtain a copy of the license at https://mozilla.org/MPL/2.0/.
```

## Install Selenium

```
pip install selenium
```

### Verify

```
$ pip show selenium 

Name: selenium
Version: 4.8.2
Summary: 
Home-page: https://www.selenium.dev
Author: 
Author-email: 
License: Apache 2.0
Location: /home/shubham/.local/lib/python3.10/site-packages
Requires: certifi, trio, trio-websocket, urllib3
Required-by: 
```

## Test the setup

A simple Python script that opens Firefox and navigates to a website.

```
touch test.py
vim test.py
```
Edit the `test.py` file and save the below script.

```
from selenium import webdriver

driver = webdriver.Firefox()
driver.get("https://www.google.com")
```

### Run

```
python3 test.py
```

![image](https://user-images.githubusercontent.com/97805339/226178876-a4344b3b-41d7-4c0f-9d4b-999b8d3d5a7d.png)

