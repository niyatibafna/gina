# Gina
#### *isi ka naam hai*

Gina is a rule-based program to build translated pairs (English to Hindi), given parallel corpora. Given corresponding English-Hindi data, she derives correspondece pairs using two things: 1) her initial lexicon, updated with every learnt pair, that 'overlaps' in newly encountered data. 2) An understanding of basic syntactical ordering in Hindi and English. 

Both of these premises place severe constraints on Gina's capacity for learning as well as her accuracy; however, this is only a rudimentary implementation of a possible approach towards lexicon building, that engages with problems such as, for example, translating from a genderless to a gendered language, or from a non-ergative to a partially ergative language. Given the simplistic setup, Gina recognizes and learns only four syntactical categories: nouns, pre/postpositions, verbs and adjectives. The approach taken, however, can be extended to certain (sub)categories (like verb auxillaries and plural nouns), but not others (like adverbs, in most cases.)

## Setup

### Authentication
Gina is still under development. You would need to setup credentials from an NLP API enabled account on GCP to get Gina up and running on your device.

### Install Dependencies
1. Install [pip](https://pip.pypa.io) and [virtualenv](https://virtualenv.pypa.io/)

2. Create a virtualenv and activate it
> ```sh
> $ virtualenv --python python3 env
> $ source env/bin/activate
> ```
If you're on Windows, you may have to specify the full path to your python installation directory
> ```sh
> $ virtualenv --python "c:\python36\python.exe" env
> $ .\env\Scripts\activate
> ```
3. Install the dependencies required by Gina
> ```sh
> $ pip install -r requirements.txt
> ```

### Run
Take a look at Gina's initial lexicon. Then give her 1) an English sentence 2) its literal Hindi translation. Try to include new words that you want her to learn, as well as old ones she can use as reference. You can check how much she has learnt from your sentece; you can also test her knowledge, and delete inaccurate deductions on her part. Teach her well!
```sh
  $ python interface.py
```

### To Do (Early 2019)
- [ ] Build a web interface for Gina
- [ ] Move to a database

### License
CC BY-NC 4.0 International
