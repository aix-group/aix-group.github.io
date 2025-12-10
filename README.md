This is the website of the xAI group at the University of Marburg.  This website is based on the minimal-mistakes jekyll theme. 

# Editors
> :warning: **Make sure you are on the `main`-branch**

> :information_desk_person: what you see in the online preview is likely not what you get

> :zzz: changes will take a few mins to take effect. Monitor progress at [actions tab](https://github.com/aix-group/xai-lab-website/actions)

## Howto...
- [manage team members](#member)
- [manage publications](#publications)

<h3 id="member">Manage Team members</h3>

Members of a group are defined in [`/_data/people.yml`](/_data/people.yml).

Example entry:
```
- name: Firstname Lastname
  mail: first.last@example.org
  roles: ['shk']
  img: LastFirst.jpg
```
#### Add Member
Add a new entry to the end of the file. See the example above or existing entries for proper format.  

Mandatory fields:
- _name:_ first and last name
- _roles:_ must be a list, even if it only has a single entry. The first entry **must** be the position in the group. Additional entries in the roles-list are optional. Possible values:
  * _shk_ - student assistant
  * _phd_ - PhD candidate
  * _extphd_ - external PhD candidate
  * _postdoc_ - Postdoctoral Researcher
  * _admin_ - Administration
  * _head_ - group leader  
  * _alumnus_ - previous group members 

Optional fields:
- mail - e-mail address, e.g. `first.last@example.org.` Multiple e-mail addresses are possible, must be provided as list, e.g., `['mail1@example.org', 'mail2@example.org']`
- _phone:_ phone nr, e.g. `+4920112345`
- _title:_ e.g. `Prof. Dr.`
- _position-special:_ more details for e.g., postdocs `Junior Research Group Lead`
- _interests:_ a list of interests, e.g. `['machine learning', 'coffe']`
- _img:_ - first, upload an image to [`/img/people`](/img/people), then provide the filename here, e.g. `LastFirst.jpg`
- _orcid:_  - orcid, pattern: 0000-000X-XXXX-XXXX
- bib: A string that can be used to filter the publication list for this person. Make sure it is unique.

<h3 id="publications">Manage Publications</h3>

Replace `references.bib` at [`/_bibliography`](/_bibliography) with your latest bibtex list of publications.

The publication list will automatically use `doi`, `url`, and `code` fields.

# Devs
The site is built with [jekyll](https://jekyllrb.com), [scholar](https://github.com/inukshuk/jekyll-scholar)-plugin and [minimal mistakes](https://mmistakes.github.io/minimal-mistakes/) theme.
## Run locally
1. Install [Ruby](https://www.ruby-lang.org)
2. Install [Bundler](https://bundler.io) `gem install bundler`
3. Checkout repo, install dependencies in the repo with `bundle install`
4. Run with `bundle exec jekyll serve`, the site is accessible at "http://127.0.0.1:4000/" (note the trailing `/`)

## Theme customization
`/sass/custom/` holds all custom adaptations



