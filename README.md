# Jux Box
> "I would not like Green eggs and ham. Would you like Green eggs and love me loud the next day you're here, one day you care. You're so unfair sipping from your cup." - Dr. Seuss, Jay Z

Jux Box is a web application that generates lyrics based off of various artists using Markov Chains. Written in Flask and deployed to Heroku. See [example here](http://juxboxhero.herokuapp.com/).

## How it works
Jux Box allows the user to select two artists then generate a random four-line lyric from the two. The lyric generation works by constructing a dictionary of words used by the artists mapped to an array of words that follow that particular word. The lyric is then generated by choosing a word from that dictionary and choosing from the list of words in it's array, then choosing the next word from our new word's array in the dictionary. By following this link you can create a whole lyric from our two artists.

## Setup
Clone this repo
```
$ git clone https://github.com/nlaz/2-chainz.git
$ cd 2-chainz
```

Install dependencies
```
$ pip install -r requirements.txt
```

Run application
```
$ python chainz.py
```

## Structure
```bash
├── lyrics/           # Folder with artists lyrics
├── README.md         # This file
├── templates/        # Handlebars HTML files
├── Procfile          # Heroku process script
├── requirements.txt  # Dependencies
├── chainz.py         # Flask routes and dictionary generation
└── static/           # Project static assets, ie. images, css, js
    ├── font/         # Font files
    ├── img/          # Images and SVGs
    └── js/           # Javascript libraries and scripts
```

## Credits
Built at [MHacks V](http://mhacksv.devpost.com/).