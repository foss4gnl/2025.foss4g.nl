# Website FOSS4GNL 2025 in Wageningen
This is the content for the website of the FOSS4GNL 2025 conference (to be) held on July 111 at the Wageningen University.

Organised together with the GeoDesk Wageningen. 

Link: https://2024.foss4g.nl

# HOW TO Creating a new website

When organizing a new FOSS4GNL create a new website as follows. In the example the new FOSS4G is in 2024, the previous in 2023. 
All edits can be done on GitHub for the initial setup and some settings are done at YourHosting.

## Github settings 

### 1. Set previous as a Template Repository
Go to the settings and mark as template. See image:

![image](https://github.com/foss4gnl/2023.foss4g.nl/assets/582630/7530c9a4-8374-4be1-8daf-ef2f2e7b5d69)

### 2. Create new Repository from Template Repo

Create a new repo called **foss4gnl/2024.foss4g.nl** from the **foss4gnl/2023.foss4g.nl** template repo. See image

![image](https://github.com/foss4gnl/2023.foss4g.nl/assets/582630/caf1a465-a3b8-4791-879f-307ef5c1a8ac)


### 3. Setup GitHub Pages for new repro
* GitHub: Fo to`Settings` of the new repro and then `Pages` 
* setup Pages to point to main branch
  
![image](https://github.com/foss4gnl/2024.foss4g.nl/assets/582630/64d6f5ec-56b4-4c12-95d9-5b983f6af0a0)

* Press `Save` now you can add the custom domain. Make this point to `foss4g.nl`

### 4. Change Github Pages for previous year 
* GitHub: Fo to`Settings` of the new repro and then `Pages` 
* GitHub: set custom domain to 2023.foss4g.nl.

### 5. Edit CNAME previous year 

* in root dir of previeous year repro , change CNAME file to 2023.foss4g.nl

## YourHosing settings

* Go to YourHosting account. 
* Go to `DNS-en redirectbeheer` then `foss4g.nl Beheer`

### 6. YourHosting CNAME changes

* At `DNS beheer:foss4g.nl` add a new CNAME  2023.foss4g.nl and point to GitHub like the CNAME 2021.foss4g.nl or other editions:

![image](https://github.com/foss4gnl/2023.foss4g.nl/assets/582630/15f4da4e-9407-4ae6-bd74-b53a461217f6)

* Press `DNS Save` 

Changes may take a while. 


That's it! Now the website should be updated

## Credits
The [2018-version of this website](https://2018.foss4g.nl) was originally made by Jasper Roest.
For [the 2019 edition](https://2019.foss4g.nl) it was further developed by Tom Commandeur @tcommandeur et al 
of TU Delft.

For the [the 2021 edition](https://2021.foss4g.nl) 2021 edition (Enschede) it was further developed by @justb4, Erik Meerburg et al.

For purposes of maintainability each FOSS4GNL site was given its own GH repo
by Just van den Broecke @justb4. 

First as https://foss4g.nl and to be later available via the URL https://2023.foss4g.nl

# Project Zeppelin / GDG DevFest 2014 site template

### About
Project Zeppelin allows you to setup awesome GDG DevFest site in 5 minutes.

Project is built on top of [Jekyll](http://jekyllrb.com/) - simple, blog-aware, static site generator. Jekyll also happens to be the engine behind GitHub Pages, which means you can use Jekyll to host your website from GitHub’s servers for free. [Learn more about Jekyll](http://jekyllrb.com/).

Template is brought by [GDG Lviv](http://lviv.gdg.org.ua/) team.

### Live demo http://gdg-x.github.io/zeppelin/

#### Automated version with Grunt <https://github.com/gdg-x/zeppelin-grunt>

### Features
* Easy to setup
* Simple and responsive design
* Integrated speakers and sessions management
* SVG icons
* SEO friendly


### Quick-start guide
1. [Fork](https://github.com/gdg-x/zeppelin/fork) this repo
2. Clone locally
3. Update ```_config.yml```
4. Select what content blocks do you need
5. Push changes to ```gh-pages``` branch
6. Enjoy your awesome DevFest site at ```http://[your github name].github.io/zeppelin/```

Or watch project presentation from [GDG[x] Townhall meeting](http://www.youtube.com/watch?v=xYmhheoLjcI). Slides available [here](https://docs.google.com/presentation/d/19aM7yNl_orDaCNND5LpCY3fShb6PyMltnzYfKvV8R_8/edit?usp=sharing)


## Local development

Check if you have [all requirements for local environment](http://jekyllrb.com/docs/installation/).
To install all development dependencies install [Bundler](http://bundler.io/).
```bash
    gem install bundler
```
and run next command from root folder:

```bash
  bundle install
```  

To start Jekyll run:
```bash
    jekyll serve -w
```
Site will be available at http://127.0.0.1:4000/zeppelin/ or http://localhost:4000/zeppelin/ (on Windows)

**NOTE:** in this mode all changes to html and data files will be automatically regenerated, but after changing ```_config.yml``` you have to restart server.

### Sass(Compass) support
**Note:** You need to install [Node.js](http://nodejs.org/download/)

To watch changes of `.sass` files and compile it to the `.css` on a fly change property `safe: true` to `safe: false` in `_config.yml`.
**Note: It works only on local machine, because GitHub runs Jekyll in `--save` [mode](https://help.github.com/articles/using-jekyll-with-pages/#configuration-overrides)**

Learn more about Sass development from [documentation](https://github.com/gdg-x/zeppelin/wiki/Sass-development).


### Resource optimizations (optional)

You can optimize images and minify css and javascript automatically (for now only on Windows).
But for Mac OS users available amazing tool - [imageoptim](https://imageoptim.com/). Thanks [@raphaelsavina](https://github.com/raphaelsavina) for link.
Optimize all images by running this script from `/automation/images/` folder:
```bash
    all_image_optimization.bat -d -jtran -pout -pquant -optip -gsicle -svgo
```

To minify CSS and JS run `minify_js.bat` (for Windows) and `minify_js.sh` (for Linux and MacOS) from `/automation/minifying/` folder:
```bash
    minify_js.bat
```

Learn more about available optimization options from [documentation](https://github.com/gdg-x/zeppelin/wiki/Resources-optimizations).

### Documentation
Quick-start guide is not enough? Checkout [full documentation](https://github.com/gdg-x/zeppelin/wiki).

### Used libraries
* [Bootstrap](https://github.com/twbs/bootstrap)
* [Animate.css](https://github.com/daneden/animate.css)
* [Waves](https://github.com/publicis-indonesia/Waves)
* [jquery.appear](https://github.com/bas2k/jquery.appear)
* [jQuery countTo Plugin](https://github.com/mhuggins/jquery-countTo)
* [Typed.js](https://github.com/mattboldt/typed.js)
* [Sticky-kit](https://github.com/leafo/sticky-kit)

### Who is using template?
Going to use template? Go on! The only thing we ask - let us know at [*lviv@gdg.org.ua*](mailto:lviv@gdg.org.ua) so we can include you to this list, or make a pull request.

| | | |
|------|------|------|
| [GDG DevFest Ukraine 2014](http://devfest.gdg.org.ua/) | [GDG DevFest Istanbul 2014](http://2014.devfesttr.com/) | [GDG Bangalore Site](http://gdgbangalore.github.io/) |
| [GDG DevFest Omsk 2014](http://gdg-devfest-omsk.org/) | [2014 南阳 GDG Devfest 大会](http://devfest.gdgny.org) | [DevFest Nordeste 2014](http://2014.devfestne.com.br/) |
| [GDG DevFest The Netherlands](http://www.devfest.nl/) | [DevFest Centro-Oeste 2014](http://www.devfestcentrooeste.com.br/) | [Android DevFest Space Coast](http://gdg-space-coast.github.io/zeppelin/) |
| [DevFest SP 2014](http://sp.devfest.com.br/) | [DevFest in Baroda](http://devfest.gdgbaroda.com/) | [GDG Hi Pic (France)](http://maximemularz.github.io/zeppelin/) |
| [GDG DevFest Córdoba 2014](http://gdgcordoba.github.io/zeppelin/) | [GDG DevFest Düsseldorf 2014](http://www.gdg-dus.de/DevFest2014/) | [GDG Makerere DevFest 2014](http://gdgmakerere.github.io/) |
| [GDG Dublin DevFest 2014](http://gdg-dublin.appspot.com/) | [GDG Busitema DevFest 2014](http://gdgbusitema.github.io/) | [DevFest Vienna 2014](http://www.devfest.at/) |
| [Android Wear DevFest](http://devfest.gdgnorthjersey.com/wear2014/) | [GDG SLAU DevFest 2014](http://gdgslau.github.io/) | [Lima DevFest](http://limadevfest.com/) |
| [GDG Korea DevFair 2014](http://devfair2014.gdg.kr/) | [GDG DevFest Kota Kinabalu 2014](http://devfest.gdgkk.info/) | [GDG DevFest Belgium](http://gdg-brussels.org/DevFest2014/) |
| [DevFest Praha 2014](http://devfest.cz/) | [GDG DevFest Kosice](http://devfest.sk/) | [GDG DevFest Cagayan de Oro](http://devfest.gdgcdo.org/) |
| [DevFest Birgunj](http://gdgbirgunj.github.io/DevFest2014/) | [GDG DevFest Poland](http://devfest.pl/) | [GDG DevFest Silicon Valley](http://devfest2014.gdgsv.com/) |
| [DevFest Chennai 2014](http://devfest.gdgchennai.com/) | [GDG DevFest Bari](http://gdgbari.github.io/zeppelin/) | [GDG DevFest Ahmedabad](http://devfest.gdgahmedabad.com/) |
| [GDG DevFest Sri Lanka](http://www.devfestlk.org/) | [GDG DevFest Tunis](http://devfest.gdgtunis.org/) | [GDG DevFest Kozhikode](http://devfest.gdgkozhikode.org/) |
| [GDG DevFest Argentina](http://devfest.gdg.com.ar/) | [GDG DevFest Bhubaneswar](http://devfest2014.gdgbbsr.com/) | [GDG DevFest Miage Gi](http://gdgmiagegilab.github.io/) |
| [GDG DevFest NORTE](http://norte.devfest.com.br/) | [GDG Devfest Nyeri 2014](http://devfest.gdgkimathiuniversity.com/) | [GDG DevFest Paris](http://devfest.gdgparis.com/) |
| [GDG Akure](http://gdgakure.github.io/)|[MENAT GDG Summit 2014](http://summit.gdg-menat.com/)|[Women Techmakers Istanbul 2015](http://2015.wtmistanbul.com) |
| [GDG DevFest Mallorca](http://devfest.gdgmallorca.com/)| [Michigan GDG DevFest 2015](http://michigandevfest.com/) | [International Women's Day](http://iwd.gdgnorthjersey.com/womeninnovation/) |
| [Women Techmakers Tbilisi 2015](http://womentechmakers.ge/) | [Android Xtended](http://www.androidxtended.com/) |[GDG Bingham University](http://binghamuni.edu.ng/gdg)|
| [JSday Maceio 2015](http://jsday.com.br) | [DevFest Nordeste 2015](http://2015.devfestne.com.br) | [GDG DevFest Vijayawada 2015](http://devfest.gdg-vijayawada.org) |
| [Geek Night Recife](http://geeknightrecife.github.io/) | [IO Extended 2016 Madrid ](http://io.gdg.es/) | [AngularCamp](http://angularcamp.org/) |
| [Mobile Era 2016](http://mobileera.rocks/) | [GDG Francisco Beltrão](http://gdg-fb.github.io) | [Women Techmakers Istanbul 2016](http://2016.wtmistanbul.com) |
| [Droidcon Paris 2015](http://droidcon.fr) | [Android Makers Paris 2017](http://androidmakers.fr) | [Heidelberger Symposium 2017](https://heidelberger-symposium.de/) |
| [DevFest Foumban website](http://devfestfoumban.org) | [NorthSec 2018](https://nsec.io/) | [SwiftFest 2018](http://swiftfest.io) |


### Contributors
* Design and web development: [Oleh Zasadnyy](https://github.com/ozasadnyy)
* Idea: [Vitaliy Zasadnyy](https://github.com/zasadnyy)

See [list of contributors](https://github.com/gdg-x/zepplin/graphs/contributors)

Maintainers: [@tasomaniac](https://github.com/tasomaniac) and [@ozasadnyy](https://github.com/ozasadnyy).

### License
Project is published under the [MIT license](https://github.com/gdg-x/zeppelin/blob/master/LICENSE.txt). Feel free to clone and modify repo as you want, but don't forget to add reference to authors :)
