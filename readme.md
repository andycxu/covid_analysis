<div id="top"></div>


<!-- PROJECT SHIELDS -->

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/rowanschaefer">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

<h3 align="center">ACT & SAT Analysis </h3>

  <p align="center">
    Completed for General Assembly DSI Immersive
    <br />
    <a href="https://github.com/rowanschaefer/act_sat_analysis"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    ·
    <a href="https://github.com/rowanschaefer/act_sat_analysis/issues">Report Bug</a>
    ·
    <a href="https://github.com/rowanschaefer/act_sat_analysis/issues">Request Feature</a>
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
    <li><a href="#datasets">Datasets</a></li>
    <li><a href="#data-dictionary">Data Dictionary</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project


Students from lower-income areas  and backgrounds have a higher barrier to achieving high scores on the SAT and ACT; in addition to systemic factors, there are also practical ones (such as the cost of re-taking the test, study materials, and tutoring.) Though this topic is already well-known and studied, this exploratory analysis intends to provide a broad overview of the relationship between SES and standardized testing outcomes in California. 
<p align="right">(<a href="#top">back to top</a>)</p>



### Built With

* [python](https://www.python.org)
* [tableau](https://www.tableau.com)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started


### Prerequisites

All you need to run this is python.
* Python
  ```sh
  pip --version
  ```

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/rowanschaefer/act_sat_analysis.git
   ```

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- DATASETS -->
## Datasets

All datasets are included in the "data" folder. 

* [`act_2019_ca.csv`](./data/act_2019_ca.csv): 2019 ACT Scores in California by School, dataset provided by General Assembly
* [`sat_2019_ca.csv`](./data/sat_2019_ca.csv): 2019 SAT Scores in California by School, dataset provided by General Assembly
* [`CA_Schools_Key.csv`](./data/CA_Schools_Key.csv): California Schools Key. This csv contains CDSCodes, city/district info, school name, and zip/coordinates for schools in CA.
* [`Education1970_to_2019.csv`](./data/Education1970_to_2019.csv): Education 1970 to 2019. This data is used to find percentages of education levels by county from 2015-2019.
* [`CA_Schools_Key.csv`](./data/CA_Schools_Key.csv): California Schools Key. This csv contains CDSCodes, city/district info, school name, and zip/coordinates for schools in CA.
* [`frpm1718.csv`](./data/frpm1718.csv): Percentages of students at each school in CA who qualified for free/reduced lunch plans, 2017-2018 school year.
* [`frpm1819.csv`](./data/frpm1819.csv): Percentages of students at each school in CA who qualified for free/reduced lunch plans, 2018-2019 school year.


<p align="right">(<a href="#top">back to top</a>)</p>



<!-- DATA DICTIONARY -->
## Data Dictionary
|      Feature     |    Type     |   Dataset   |       Description              |
|---|---|---|---|
| **mini_cds**   |  *integer*  | 2010 census | The last 6 digits from a California School Code or CDS (City, District, School) code. Used to join dataframes. | 
| **school**  |  *object*    | 2010 census | Name of the school. Includes high schools in CA |
| **school_type**  |  *object*    | 2010 census | Type of school - i.e. charter schools, private, public. |
| **county**  |  *object*    | 2010 census | Name of the county the school is located in |
| **free_meal_eligibility**  |  *float*    | 2010 census | Percentage of students who qualified for free meals, average of years 2018 and 2019. |
| **freereduced_eligibility**  |  *float*    | 2010 census | Percentage of students who qualified for free or reduced meal plans, average of years 2018 and 2019.|
|    |    |   | *note, these two categories are not mutually exclusive.*|
| **sat_pct_math_benchmark**  |  *float*    | 2010 census | Percentage of students (both grade 11 and 12) who met the math benchmark on the SAT |
| **sat_pct_erw_benchmark**  |  *float*    | 2010 census | Percentage of students (both grade 11 and 12) who met the reading/writing benchmark on the SAT  |
| **act_pct_21**  |  *float*    | 2010 census | Percentage of students at the school who scored a 21 or higher on the ACT |
| **act_avgscore**  |  *float*    | 2010 census | Average ACT score of all students at the school |
| **act_avg_read**  |  *float*    | 2010 census | Average ACT reading subscore of all students at the school |
| **act_avg_math**  |  *float*    | 2010 census | Average ACT math subscore of all students at the school |
| **act_avg_sci**  |  *float*    | 2010 census | Average ACT science subscore of all students at the school |
| **act_avg_eng**  |  *float*    | 2010 census | Average ACT english subscore of all students at the school |
| **county_no_hs**  |  *float*    | 2010 census | Percent of adults living in the given county who do not have a high school diploma |
| **county_hs_only**  |  *float*    | 2010 census | Percent of adults living in the given county who have only a high school diploma |
| **county_somecollege**  |  *float*    | 2010 census | Percent of adults living in the given county who have an associate's degree or some college |
| **county_bachelorsplus**  |  *float*    | 2010 census | Percent of adults living in the given county who have a a bachelor's degree or higher|
| **zip**  |  *object*    | 2010 census | 5 or 10-digit zipcode of school |
| **latitude**  |  *float*    | 2010 census | latitude coordinates of school, used for mapping in tableau |
| **longitude**  |  *float*    | 2010 census | longitude coordinates of school, used for mapping in tableau |


<!-- CONTRIBUTING -->
## Contributing

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Rowan - [@rowanschaefer](https://linkedin.com/in/rowanschaefer) - rgscha02@gmail.com

Project Link: [https://github.com/rowanschaefer/act_sat_analysis](https://github.com/rowanschaefer/act_sat_analysis)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* *thanks for the readme template [othneildrew](https://github.com/rowanschaefer/Best-README-Template)
* *thanks ben for helping me with that code I couldn't figure out

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/github_username/repo_name.svg?style=for-the-badge
[contributors-url]: https://github.com/github_username/repo_name/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/github_username/repo_name.svg?style=for-the-badge
[forks-url]: https://github.com/github_username/repo_name/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo_name.svg?style=for-the-badge
[stars-url]: https://github.com/github_username/repo_name/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo_name.svg?style=for-the-badge
[issues-url]: https://github.com/github_username/repo_name/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo_name.svg?style=for-the-badge
[license-url]: https://github.com/github_username/repo_name/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/linkedin_username
[product-screenshot]: images/screenshot.png

