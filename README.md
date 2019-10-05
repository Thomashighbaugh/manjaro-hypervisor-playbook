<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]
![SpaceMacs][spacemacs-logo]


<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/Thomashighbaugh">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/24/Ansible_logo.svg/832px-Ansible_logo.svg.png" alt="Logo" width="80" height="80">
  </a>

  <h1 align="center">Manjaro Workstation Playbook</h1>

  <p align="center">
My personal configurations of my Manjaro workstation, WM independent. 
    <br />
    <br />
    <br />
    =
    <a href="https://github.com/othneildrew/Best-README-Template/issues">Report Bug</a>
    =
    <a href="https://github.com/othneildrew/Best-README-Template/issues">Request Feature</a>
    = 
  </p>



<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Playbook](#about-the-playbook)
  * [Built With](#built-with)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Usage](#usage)
* [Roadmap](#roadmap)
* [License](#license)
* [Acknowledgements](#acknowledgements)


[![Product Name Screen Shot][product-screenshot]](https://example.com)

<!-- ABOUT THE PROJECT -->
## About The Playbook
<br/>
 This is the result of my frustrations with the BASH scripts I was using to provision my
 workstation since moving to ZSH as my primary shell and seeing a well structured Arch 
based configuration that demonstrated several features of **Ansible** I was unaware of 
when using it for provisioning VM servers prior. The Spark Playbook does an excellent 
job demonstrating all of the key features of Ansible that were holding back my internal 
deployment thereof prior and without yodeling its specific jargon in an abstracted way 
that I personally find rather hard to learn while attempting to comprehend the 
underlying technology. 

### Built With
This project leverages the power of Ansible to take the place of the several scripts that I had been using prior to reprovision my workstation after my experiments with Linux lead to their inevitable outcome, breaking the install. 

Ansible is an application of YAML markup to automate redundant aspects of system provisioning that can scale out to entire networks of servers requiring identical, or similar, post-installation states. This technology is developed by Red Hat, who offer extensive (albeit jargon intensive) documentation and "_getting started_" videos on the topic for those seeking more information.

#### Structural Considerations
The biggest selling point for me about using Ansible in this project was the modular nature of the 
project which I based this effort on, having a similar modular structure that I have taken to 
in creating websites with React (or PHP) and styling them with SCSS. 

Having each task as its own directory that contains directories and files related to that 
task make the code reusable in other applications which prevents redundant efforts and allows 
for a better debugging experience in general. 


<!-- GETTING STARTED -->
## Getting Started
To use this playbook, it is advised that you begin with a freshly installed Manjaro system, which is what it is tested against using both AwesomeWM or i3 (depending on my mood when installing). At minimum, an operating system that has pacman as its package manager is needed to take advantage of this playbook and due to the idempotent (aka can install on top of existing systems) nature of Ansible it _should not_ destroy your OS. 
### Prerequisites

```sh
# install the dependencies 
$ sudo pacman -S python-passlib ansible

# download this repo
git clone https://github.com/Thomashighbaugh/
```

### Installation

```sh
# run the playbook from the directory 
## Use sudo instead of running as su for single deployment of yay
sudo ansible-playbook -i localhost playbook.yml

```

<!-- USAGE EXAMPLES -->
## Usage
This project can be used to provision your own system or as the basis for your own custom playbook to provision a system to your specific use case. 

In addition, the tasks are modularized in such a way that individual tasks can easily be used as pieces of another playbook without more than adding them to the playbook.yml file you create. 

### AUR Solution
Due to AUR helpers not allowing themselves to be run as root, I have included a temporary solution until I have a crack at the AUR helper roles available or write a role for this purpose. My solution uses AURA, another AUR helper that allows itself to run as root. 

Where AUR packages are needed, I call AURA as a shell command, which isn't the most elegant solution but until I have time to sort out the nightmare of AUR helpers and Ansible, it works. 

<!-- ROADMAP -->
## Roadmap
If you want to reccomend any features or tasks of this playbook, or spot some glaring flaw in it, feel free to open an issue and I will address it directly. 



<!-- LICENSE -->
## License

Distributed under the MIT License. Feel free to use it at your own risk and for whatever purposes you see fit in accordance with the terms of that license. 


<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [Ansible](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Ansible Module for Pacman](https://shields.io)
* [Ansible AUR Module](https://choosealicense.com)
* [Spark Playbook](https://pages.github.com)
* [Manjaro i3 Module](https://daneden.github.io/animate.css)
* [Best README Template](https://github.com/othneildrew/Best-README-Template/blob/master/README.md)





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=flat-square
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=flat-square
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=flat-square
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=flat-square
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=flat-square
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
[spacemacs-logo]: https://cdn.rawgit.com/syl20bnr/spacemacs/442d025779da2f62fc86c2082703697714db6514/assets/spacemacs-badge.svg
 
