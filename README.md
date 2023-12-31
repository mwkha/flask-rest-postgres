<!-- README template from: https://github.com/othneildrew/Best-README-Template -->
<a name="readme-top"></a>


<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="hhttps://github.com/mwkha/flask-rest">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

<h3 align="center">Flask app capturing REST api calls cars and car sales details via REST api's into postgres db</h3>

  <p align="center">
    Flask app that captures car details and car sales details via REST api's and stores them into a postgres db.
    <br />
    <a href="https://github.com/mwkha/flask-rest"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/mwkha/flask-rest">View Demo</a>
    ·
    <a href="https://github.com/mwkha/flask-rest/issues">Report Bug</a>
    ·
    <a href="https://github.com/mwkha/flask-rest/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][product-screenshot]](https://example.com)

Here's a blank template to get started: To avoid retyping too much info. Do a search and replace with your text editor for the following: `mwkha`, `flask-rest`, `twitter_handle`, `linkedin_username`, `email_client`, `email`, `project_title`, `project_description`

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple example steps.

### Prerequisites

The project uses python, insomnia for requests and postgres using docker OR brew.
* docker for macOS
  ```sh
  brew install docker
  ```
* python for macOS
  ```sh
  brew install python
  ```
* insomnia for macOS
  ```sh
  brew install --cask insomnia
  ```
* OPTIONAL postgres and pgadmin4 via brew (If using docker don't need this)
  ```sh
  brew install postgresql@14
  brew install --cask pgadmin4
  ```
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->
## Usage

* Ensure .env db url is using host.docker.internal as below
  ```sh
  DATABASE_URL=postgres://user:pwd@host.docker.internal:5432/test_db
  ```
* Configure docker-compose postgres username, password and db name then run
  ```sh
  docker-compose up -d
  docker-compose ps
  ```
* POST requests can be made to endpoints 
  ```sh
  /api/car accepts json format "{'brand' : 'mazda'}"
  /api/transaction accepts json format "{'car_id' : 1, 'sale_price' : 30000}"
  ```
* To enter into postgres service running in docker use
  ```sh
  docker-compose exec postgres psql --username=ENTER_USERNAME --dbname=ENTER_DB_NAME
  ```
* Useful commands inside postgres
  ```sh
  \l # to list all databases
  \c db_name # connect to database db_name
  \dt # to list all tables within the database after connection
  \conninf # to list the current conncection info, database, user and port
  \du # ist all roles created
  ```

## OPTIONAL 1 running app locally + postgres via docker
* Install requirements.txt file by running
  ```sh
  pip3 install -r requirements.txt
  ```
* Update .env file to use localhost instead of host.docker.internal
  ```sh
  DATABASE_URL=postgres://user:pwd@localhost:5432/test_db
  ```
* Update .env file to use localhost instead of host.docker.internal


## OPTIONAL 2 running both app + postgres locally.
* Install requirements.txt file by running
  ```sh
  pip3 install -r requirements.txt
  ```
* Start postgres service locally
  ```sh
  ./services.sh start
  psql postgres
  CREATE ROLE newUser WITH LOGIN PASSWORD ‘password’; # Create new user with pwdd
  ALTER ROLE newUser CREATEDB; # Allow new user to create databases
  \q # Quit current session
  psql postgres -U newuser # Login with new user 
  \conninfo # Check the current connection details.
  ```

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [ ] Feature 1
- [ ] Feature 2
- [ ] Feature 3
    - [ ] Nested Feature

See the [open issues](https://github.com/mwkha/flask-rest/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Your Name - [@twitter_handle](https://twitter.com/twitter_handle) - email@email_client.com

Project Link: [https://github.com/mwkha/flask-rest](https://github.com/mwkha/flask-rest)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* []()
* []()
* []()

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/mwkha/flask-rest.svg?style=for-the-badge
[contributors-url]: https://github.com/mwkha/flask-rest/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/mwkha/flask-rest.svg?style=for-the-badge
[forks-url]: https://github.com/mwkha/flask-rest/network/members
[stars-shield]: https://img.shields.io/github/stars/mwkha/flask-rest.svg?style=for-the-badge
[stars-url]: https://github.com/mwkha/flask-rest/stargazers
[issues-shield]: https://img.shields.io/github/issues/mwkha/flask-rest.svg?style=for-the-badge
[issues-url]: https://github.com/mwkha/flask-rest/issues
[license-shield]: https://img.shields.io/github/license/mwkha/flask-rest.svg?style=for-the-badge
[license-url]: https://github.com/mwkha/flask-rest/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/linkedin_username
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 