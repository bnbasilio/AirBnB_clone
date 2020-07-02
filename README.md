# This file lists all individuals having contributed content to the repository.

Nic Basilio <1451@holbertonschool.com>
Samuel Pomeroy <samuel.m.pomeroy@gmail.com>
vagrant@vagrant-ubuntu-trusty-64:~/HBnB-draft$ cat README.md
# **0x00. AirBnB clone - The console**


## Description
The first in a series of projects that will ultimately lead to a clone of a past version of AirBnB. We were tasked with building a set of classes, each with attributes corresponding to various types of data needed for listings on the final website; a file storage engine to record those objects in a JSON file; and an interactive console to manage that storage.

## Using the console:

From project directory: `./console.py`

## Implemented console commands:
| command | functionality |
| --- | --- |
| quit | Same as default, quits interpreter. |
| EOF | (Ctrl + d) to quit |
| create | Creates a new object of the specified class, and returns its id. |
| show | Prints information about the specified object and its attributes. |
| destroy | Deletes object of specified id. |
| all | With no args, shows all objects, or all objects of a specified type. |
| update | Adds or updates the specified attribute for the specified object. |

## Examples from console:

`(hbnb) quit`

`$`

--

`(hbnb) EOF`

`$`

--

`(h-bnb) <ctrl + d>`

`$`

--

`(hbnb) create BaseModel`

`49faff9a-6318-451f-87b6-910505c55907`

`(hbnb) `

--

`(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907`

`[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'first_name': 'Betty', 'id': '49faff9a-6318-451f-87b6-910505c55907', 'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 3, 49401)}`

--

`(hbnb) create BaseModel`

`2dd6ef5c-467c-4f82-9521-a772ea7d84e9`

`(hbnb) all BaseModel`

`["[BaseModel] (2dd6ef5c-467c-4f82-9521-a772ea7d84e9) {'id': '2dd6ef5c-467c-4f82-9521-a772ea7d84e9', 'created_at': datetime.datetime(2017, 10, 2, 3, 11, 23, 639717), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 23, 639724)}", "[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'first_name': 'Betty', 'id': '49faff9a-6318-451f-87b6-910505c55907', 'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 3, 49401)}"]`

`(hbnb) all`

`["[BaseModel] (2dd6ef5c-467c-4f82-9521-a772ea7d84e9) {'id': '2dd6ef5c-467c-4f82-9521-a772ea7d84e9', 'created_at': datetime.datetime(2017, 10, 2, 3, 11, 23, 639717), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 23, 639724)}", "[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'first_name': 'Betty', 'id': '49faff9a-6318-451f-87b6-910505c55907', 'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 3, 49401)}"]`

--

`(hbnb) destroy BaseModel 49faff9a-6318-451f-87b6-910505c55907`

`(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907`

`** no instance found **`

`(hbnb) `

--

`(hbnb) update BaseModel 2dd6ef5c-467c-4f82-9521-a772ea7d84e9 test "123"`

`(hbnb) show BaseModel 2dd6ef5c-467c-4f82-9521-a772ea7d84e9`

`[BaseModel] (2dd6ef5c-467c-4f82-9521-a772ea7d84e9) {'id': '2dd6ef5c-467c-4f82-9521-a772ea7d84e9', '
test': '123', 'created_at': datetime.datetime(2017, 10, 2, 3, 11, 23, 639717), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 23, 639724)}`

--

## File List

| File Name | Description |
| --- | --- |
| `console.py` | Our interpreter for managing `BaseModel` and `BaseModel` child class objects recorded in a JSON file. |
| `models/__init__.py` | The only `__init__.py` with content, this creates the `FileStorage` object used to store all our other objects, and loads into it the JSON file contents. |
| `models/base_model.py` | Governs instantiation of all `BaseModel` child classes: |
| `models/user.py` | Defines `BaseModel.User` object. |
| `models/state.py` | Defines `BaseModel.State` object. |
| `models/city.py` | Defines `BaseModel.City` object. |
| `models/amenity.py` | Defines `BaseModel.Amenity` object. |
| `models/place.py` | Defines `BaseModel.Place` object. |
| `models/review.py` | Defines `BaseModel.Review` object. |
| `models/engine/__init__.py` | Empty, only needed for package structure. |
| `models/engine/file_storage.py` | Defines `FileStorage` class and all its methods used to manage storage via the console. |
| `tests/__init__.py` | Empty, only needed for package structure. |
| `tests/test_base_model.py` | Test suite for `base_model.py`. |
| `tests/test_engine/__init__.py` | Empty, only needed for package structure. |
| `tests/test_engine/test_file_storage.py` | Test suite for `file_storage.py`. |

## Development Environment
Tested on Ubuntu 14.04 LTS, built in Python 3.4.3 [GCC 4.8.4].

## Styling
All files have been written in the Pep8 style.

## Authors
* **Nic Basilio** - [bnbasilio](https://github.com/bnbasilio)
* **Samuel Pomeroy** - [allelomorph](https://github.com/allelomorph)
