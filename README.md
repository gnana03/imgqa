[![Waffle.io - Columns and their card count](https://badge.waffle.io/pyqa/imgqa.svg?columns=all)](https://waffle.io/pyqa/imgqa)
[![Build Status](https://travis-ci.org/pyqa/imgqa.svg?branch=master)](https://travis-ci.org/pyqa/imgqa)
[![PyPI version](https://badge.fury.io/py/imgqa.svg)](https://badge.fury.io/py/imgqa)

# QA automation framework - QA Re-Imagined!

QA-ReImagined a.k.a `IMGQA` is a unified test automation framework based on python. This has come up after thoroughly study made on existing methodologies used in majority of projects for UI/Rest API testing, This is expected to solve a list of problem statements readily.
The framework aims to be a constructive blend of various guidelines, coding standards, concepts, processes, practices, project hierarchies, modularity, reporting mechanism, test data injections etc., to pillar automation testing.


## Key Features

- **Selenium functions:** This module contains a good number of Selenium wrapped functions which are commonly used for UI Testing. These wrapped functions provide a shield of exception handling over the regular selenium methods, handling all different kinds of exception that can occur. If due to some reason, any of the provided method doesnot work, then there is a provision of fall back mechanism, provided in each method, by leveraging additional technologies/javascript 
 
- **Rest API functions:** This module contains Rest API wrapped functions which are commonly used for Rest API Testing, by leveraging python 'requests' library. The methods are generalized, to handle any kind of request like GET, PUT, POST, DELETE etc. The module has provison to manage the authentication token. Additionally, there are generic methods for commonly used assertion types and for validating the parameters, that come along with a request like headers, payload etc. in a most possible simplified manner
 
- **Utilities:** This module aims to provide community backed utility libraries built with a focus on reusability. Following are the utilities, currently supported by the framework:  
    - **Image Comparison:** This module provides provision for image comparison through openCV, SSIM(Structured similarity index) as opposed to pixel by pixel comparison. The methods are generic and need just 2 images to compute the difference. 
     
    - **Captcha Reading:** This utility performs the captcha reading from an image, by leveraging the 'pytesseract' module. It takes an image as input, containing captcha, and returns a string, mentioning the captcha.
     
    - **Spell Check, Accessibility Check in web application:** This module is in WIP mode, where we are enabling spell checks and accessibility checks in web applications, by leveraging the web spider concept, which browses the World Wide Web in a methodical, automated manner, takes out all the links from a web page so that the process could be repeated.

- **Reporting:** The framework is flexible enough to work with multiple reporting platforms like `reportportal.io`, `allure-report` etc. A regular, self-contained and customizable HTML report can also be generated through the use of `pytest-html` module.(which is bundled as a dependency for this package)
 
- **Continuous Testing:** The framework provides the facility for CT(Continuous Testing) by leveraging Docker. The docker file provided in the framework can be used to setup the necessary prerequisites/environment, needed to run the framework, on any server, from scratch. 

## Prerequisites

The framework requires 
- [python 2.7+ / 3.6+](https://www.python.org/downloads/)
- [pip](pip )
- [pytest](https://docs.pytest.org/en/latest/getting-started.html) to be installed in the machine.

## Installing

Valid/Tested Version is suggested to be installed directly from PyPi as it will solve the issue of dependencies automatically.

`pip install imgqa`

In case of any custom updates done to the current setup,we will need to clone the current repository and run `python setup.py develop` so that the local changes are reflected in the install version.


## Running the tests

The sample test cases for all the features are listed under **imgqa --> Examples** folder. To run the sample tests, open command prompt/terminal, go to imgqa --> Examples folder and run the following command:

`pytest {filename}.py -s` (-s indicates the standard output, please refer [here](https://docs.pytest.org/en/latest/contents.html) for a detailed understanding around pytest framework and its features/plugins/options etc.)

