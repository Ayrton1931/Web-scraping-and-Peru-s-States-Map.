# Web-scraping-and-Peru-s-States-Map.
R. This code download Agricultural Budget of SIAF at states level, then graph the distribution in a Peru Map. This code use "rnaturalearth"packages 
to get Peru's Map.
For use Rselenium is important to make this steps (Just do it if your computer does not have windows professional).

##### (1) Donwload Selenium from 'https://www.selenium.dev/downloads/' (jar selenium-server-standalone-x.xxx.xx)
##### (2) Donwload exe file from "https://github.com/mozilla/geckodriver/releases", for FIREFOX 
##### (3) Open cmd.exe of OS. 
##### (4) On cmd define folder where there is the selenium file and 
#####     Put 
#####     java -Dwebdriver.gecko.driver="C:\Program Files\Selenium\geckodriver-v0.26.0-win64\geckodriver.exe" -jar selenium-server-standalone-3.141.59.jar 

Other import indication is configure Firefox profile to donwload documents.
Some website to get information about that:
http://www.seleniumframework.com/intermediate-tutorial/firefox-profile/
https://www.toolsqa.com/selenium-webdriver/how-to-download-files-using-selenium/

fprof <- makeFirefoxProfile(list(browser.download.dir = path_donwload, #### Definition of download folder path  
                                 browser.download.folderList = 2L, 
                                 browser.helperApps.neverAsk.openFile = "text/csv,application/ms-excel,application/download", ### Type of file that will be donwload
                                 browser.helperApps.neverAsk.saveToDisk="application/ms-excel,application/download" ### Type of file that will be donwload. There are many types, specify before run it
                                 )
                            )  
