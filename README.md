## coursera-downloader
script for downloading coursera enrolled courses

This script is modified form of https://github.com/jansenicus/www-coursera-downloader/blob/master/WWW-COURSERA-DOWNLOADER.ipynb
somehow,
"sectionsection[[chosen_coursechosen_c -1].click()" was not working for me.

Note: If some of the packages of python is not installed, then RUN "!pip install name of package " in jupyter notebook.

I am using chrome webdriver

### How to install chrome webdriver
- You can install in linux using this commands

```
$ cd $HOME/Downloads
$ wget https://chromedriver.storage.googleapis.com/2.37/chromedriver_linux64.zip
$ unzip chromedriver_linux64.zip
$ mkdir -p $HOME/bin
$ mv chromedriver $HOME/bin
$ echo "export PATH=$PATH:$HOME/bin" >> $HOME/.bash_profile
```

  
- For other os or for more details visit [this link](http://splinter.readthedocs.io/en/latest/drivers/chrome.html)

### How to use it::
- Edit 'course title' is the name of folder which you want create and download all course content in it.
- Edit the 'course_link' to one of courses you want to download it (In order to download it you should enroll in that course first)
- Final download link will be current directory (where jupyter is running) + folder name
```
# give name of where you want to download
course_title="neural-networks-deep-learning"
# give the link of course in which you are enrolled and you want to download
course_link="https://www.coursera.org/learn/neural-networks-deep-learning/home/welcome"
lecture_homepage = browser.driver.current_url
browser.visit(course_link)

create_download_dir(course_title)
screenshot()
```

Note:- If downloading stop in between, Re-run download part jupyter cell
