## Simplify :pen:

<p align="center">
     Simplify is a Chrome Extension that summarizes any article you're reading in just one click! 
     <br/>
     It calls on an API that was made and deployed on Herkou to get the summary of the article.
</p>


## Motivation

>  The advent of the 21st century has ushered in the information era. Our race has evolved to process mountains of information every day. However, the attention spans of future generations are steadily decreasing. To combat this, we have created Simplify, an innovative tool that allows humans to process large amounts of information at lightning speeds.



## Screenshots

<p align="center">
     <img  src="./readme_imgs/logo.jpg" alt="demo">
</p>

<p align="center">
     <img  src="./readme_imgs/demogif.gif" alt="demo">
</p>



## Technologies Used

- [Newspaper3k](https://newspaper.readthedocs.io/en/latest/)
- [Flask](https://flask.palletsprojects.com/en/1.1.x/)
- [Herkou](https://www.heroku.com//)
- Vanilla Javascript, HTML, and CSS



## Installation

The Developers couldn't get this on the Chrome Extension Store, so here are the steps to add it to yourself!

1. clone this repo. on your local machine (git clone https://github.com/MLH-Fellowship/Simplify.git)
2. type `chrome://extensions` into Google Chrome and on the top right, turn on developer mode

<p align="center">
     <img  src="./readme_imgs/installation_toggle.PNG" alt="demo">
</p>

3. on the top left, press `Load unpacked`

<p align="center">
     <img  src="./readme_imgs/installation_load.PNG" alt="demo">
</p>

4. in the directory where you saved this repo. and select the `src` folder

<p align="center">
     <img  src="./readme_imgs/file_example.PNG" alt="demo">
</p>

5. you can now use our extension!

<p align="center">
     <img  src="./readme_imgs/installation_done.PNG" alt="demo">
</p>

## How to Use?

1. Open an article on your browser
2. Click the Simplify Extension

<p align="center">
     <img  src="./readme_imgs/usage_exten.png" alt="demo">
</p>

3. Read the summary

<p align="center">
     <img  src="./readme_imgs/usage_summary.jpg" alt="demo">
</p>

## API Reference

### Usage

URL: https://summary-api-zzranger.herokuapp.com/

##### Endpoint

`GET` https://summary-api-zzranger.herokuapp.com/query?article=`{articleUrl}`

> Gets the summary for the article located at `articleUrl`



##### Parameters

`{articleUrl}`

> The URL of the article you want the summary of



##### Sample Request

```
curl -I -X GET "https://summary-api-zzranger.herokuapp.com/query?article=https://stories.mlh.io/the-mlh-fellowship-is-back-this-fall-eedc9ffa7874"
```

> Getting the summary from https://stories.mlh.io/the-mlh-fellowship-is-back-this-fall-eedc9ffa7874



##### Sample Response

```json
{
  "summary": "Our first MLH Fellowship, launched back in May, had nearly 20,000 amazing applicants from around the world.\nWe are now publishing our forward-looking schedule with a Fall 2020, Spring 2021, and Summer 2021 Fellowship already in the works.\nWe look forward to seeing all of the amazing applicants for our Fall 2020 MLH Fellowship batch and as always, we can’t wait to see what you build."
}
```

##### Response Definitions

`summary` 

> Summary of the article located at `articleUrl`


### Installation

Follow these steps if you want to run the API locally

1. Open the root directory (should be the Simplify folder)
2. Navigate to the heroku folder (cd heroku)
3. Install the necessary libraries (pip install -r requirements.txt)
4. Run the flask server (python wsgi.py)

The API will now run on localhost:9874. Follow the API reference above to get article summaries (replace domain name w/ localhost).

Example

``` http://localhost:9874/query?article=https://www.cnn.com/politics/live-news/election-results-and-news-11-09-20/index.html ```


## Other


Devpost Submission: https://devpost.com/software/simplify-cvn8mg

Text_Summarizer_Models.ipynb: This Jupyter notebook contains the BART text-summarization model, which the team is currently investigating. We plan on implementing either this particular model or something similar to handle text-summarization over newspaper3k.


## Made with ❤️ by Pod 1.1.6 - the Git Geese:
|                       Cirill Dalangin                        |                         Clara Chick                          |                          Caleb Lim                           |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| [<img src="https://avatars2.githubusercontent.com/u/40480780?s=460&u=8c1edf8c533e2fb0a97dfce1342fcf2960a12c1b&v=4" width="100px;"/>](https://florenz.tech/)<br />[🌍](https://florenz.tech/) [💻](https://github.com/cdalangin) [🤝](https://www.linkedin.com/in/cfdalangin/) | [<img src="https://media-exp1.licdn.com/dms/image/C4E03AQE8eYc0h_TPHg/profile-displayphoto-shrink_400_400/0/1601867978161?e=1614211200&v=beta&t=XI_DHB1EgHoKLIndAI7vaup-M25lmVnp1l2fn_M9E04" width="100px;"/>](https://clarachick.me/)<br />[🌍](https://clarachick.me/) [💻](https://github.com/KohinaTheCat) [🤝](https://www.linkedin.com/in/clarachick/) | [<img src="https://avatars2.githubusercontent.com/u/47403443?s=460&v=4" width="100px;"/>](https://github.com/ZzRanger)<br /> [💻](https://github.com/ZzRanger) [🤝](https://www.linkedin.com/in/caleb-lim-b243a61ba/) |
