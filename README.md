# _Python Automation Base._
_The aim of the '''Python Automation Framework''' is to provide a set of tools and best practices to write automation tests scripts regarding to UI and Services. In the following sections the tools and practices will be described as well as a guide to create a script._

#### _Version._
_2.0.2_

#### _Install._
_git clone https://jorgeloviedo@bitbucket.org/jorgeloviedo/automation.git automation_

_The project provides tutorials and examples. Therefore, it should not be installed. To prepare the local installation, use the following command to install all prerequisites:_

* _[Upgrading Pip]_ - _Pip is already installed, but you'll need to upgrade pip._
* _[Virtual Environment]_ - _Creating Virtual Environments._
* _[Requirements Files]_ - _The common scenario is to install from PyPI using Requirement Specifiers._

        pip install -r requirements.txt

#### _Directory Layout  Structure._
![Layout](images/layout.png)

* _[Behave Layout Variations]_ - _Feature Testing Layout._

#### _Page Object Design Pattern._
_Page Object is a Design Pattern which has become popular in test automation for enhancing test maintenance and reducing code duplication. A page object is an object-oriented class that serves as an interface to a page of your AUT. The tests then use the methods of this page object class whenever they need to interact with the UI of that page. The benefit is that if the UI changes for the page, the tests themselves don’t need to change, only the code within the page object needs to change. Subsequently all changes to support that new UI are located in one place._

* _[Best Practices]_ - _Best Practices._
* _[Page Object Design]_ - _Page Object Design Example._

#### _Library Information._
* _[Setuptools]_ - _Easily download, build, install, upgrade, and uninstall Python packages._
* _[Pip]_ - _Tool for installing Python packages._
* _[Behave]_ - _Framework behaviour-driven development._
* _[Pep8]_ - _Python style guide checker._
* _[Flake8]_ - _The modular source code checker: pep8, pyflakes and co._
* _[Hamcrest]_ - _Framework for writing matcher objects._
* _[Selenium]_ - _A browser automation framework and ecosystem._

#### _Logging Levels._
_The numeric values of logging levels are given in the following table. These are primarily of interest if you want to define your own levels, and need them to have specific values relative to the predefined levels. If you define a level with the same numeric value, it overwrites the predefined value; the predefined name is lost._

* _[Logging Levels]_ - _Logging Levels Details._

#### _Expected Conditions._
_There are some common conditions that are frequent when automating web browsers. Listed below are Implementations of each. Selenium Python binding provides some convienence methods so you don’t have to code an expected_condition class yourself or create your own utility package for them._

* _[Expected Conditions]_ - _Expected Conditions Details._

#### _LogRecord attributes._
_The LogRecord has a number of attributes, most of which are derived from the parameters to the constructor. (Note that the names do not always correspond exactly between the LogRecord constructor parameters and the LogRecord attributes.) These attributes can be used to merge data from the record into the format string. The following table lists (in alphabetical order) the attribute names, their meanings and the corresponding placeholder in a %-style format string._

* _[LogRecord Attributes]_ - _LogRecord attributes Details._

#### _How run the features._
_In the automation directory (where the file behave.ini exist) run the file of features required._

_Example._

    user@pcname /d/automation (master)
    $ behave -v -D foo=bar web_section/features/name.feature

_Define user-specific data for the config.userdata dictionary._

    Example: -D foo=bar to store it in config.userdata["foo"].

_For more information search into in configuration.py file._

#### _How Use Pip._
    pip freeze --local | grep -v '^\-e' | cut -d = -f 1  | xargs pip install -U

#### _How User Flake8._
    flake8 common
    flake8 web
    flake8 web --ignore E501
    flake8 web --ignore E501,F811

#### _More About Selenium._
* _[SeleniumHQ]_ - _Encapsulating a variety of tools and libraries enabling web browser automation._

#### _More About Behave._
* _[Using]_ - _Command-Line Arguments._
* _[Gherkin Language]_ - _Gherkin language support._
* _[Spoken Languages]_ - _Supports over 60 spoken languages and the number is steadily growing._
* _[Formatters and Reporters]_ - _Two different concepts for reporting results of a test run._
* _[Pdf Documentation]_ - _Benno Rice, Richard Jones and Jens Engel (Release 1.2.6.dev0)._
* _[Predefined Data Types]_ - _Parse types list supported in step definitions without registration._

#### _Driver Information._
* _[Chromium]_ - _List of Command Line Switches._
* _[Chrome Driver]_ - _Storage._
* _[Chrome Driver Setting]_ - _Capabilities & ChromeOptions._
* _[Desired Capabilities]_ - _Capabilities & ChromeOptions._
* _[Marionette]_ - _Marionette, the next generation of FirefoxDriver._


#### _License._
_Copyright (c) 2016 Vates._

_Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:_ 

_The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software._

_THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE._

   [Upgrading Pip]: <https://pip.pypa.io/en/stable/installing/#upgrading-pip>
   [Virtual Environment]: <https://packaging.python.org/installing/#creating-and-using-virtual-environments>
   [Pip]: <https://pypi.python.org/pypi/pip>
   [Behave]: <https://github.com/behave/behave>
   [Setuptools]: <https://bitbucket.org/pypa/setuptools>
   [Pep8]: <https://pypi.python.org/pypi/pep8>
   [flake8]: <https://pypi.python.org/pypi/flake8>
   [Hamcrest]: <http://hamcrest.org/>
   [Selenium]: <http://docs.seleniumhq.org/docs/>
   [Page Object Design]: <http://www.seleniumhq.org/docs/06_test_design_considerations.jsp#page-object-design-pattern>
   [Behave Layout Variations]: <http://pythonhosted.org/behave/gherkin.html#layout-variations>
   [Logging Levels]: <https://docs.python.org/2/library/logging.html#logging-levels>
   [Requirements Files]: <https://pip.pypa.io/en/latest/user_guide/#requirements-files>
   [Expected Conditions]: <http://selenium-python.readthedocs.org/waits.html#explicit-waits>
   [LogRecord Attributes]: <https://docs.python.org/2/library/logging.html#logrecord-attributes>
   [Best Practices]: <http://www.slisenko.net/2014/06/22/best-practices-in-test-automation-using-selenium-webdriver/>
   [Using]: <http://pythonhosted.org/behave/behave.html#configuration-file>
   [Gherkin Language]: <https://github.com/mackoj/language-gherkin-i18n>
   [Spoken Languages]: <https://github.com/cucumber/cucumber/wiki/Spoken-languages>
   [Chromium]: <http://peter.sh/experiments/chromium-command-line-switches/>
   [Chrome Driver]: <http://chromedriver.storage.googleapis.com/index.html>
   [Chrome Driver Setting]: <https://sites.google.com/a/chromium.org/chromedriver/capabilities>
   [Desired Capabilities]: <https://github.com/SeleniumHQ/selenium/wiki/DesiredCapabilities>
   [SeleniumHQ]: <https://github.com/SeleniumHQ/selenium/>
   [Formatters and Reporters]: <https://pythonhosted.org/behave/formatters.html>
   [Pdf Documentation]: <https://media.readthedocs.org/pdf/behave/latest/behave.pdf>
   [Predefined Data Types]: <https://pythonhosted.org/behave/parse_builtin_types.html>
   [Marionette]: <https://developer.mozilla.org/en-US/docs/Mozilla/QA/Marionette/WebDriver>
