# ML book

```{epigraph}
We are drowning in information and starving for knowledge.

-- Rutherford D. Roger
```

The amount of information is enormous nowadays and it is continuously growing. See [resources](./resources.md) to observe only a tiny fraction of machine learning content available on the Web. Isn't it enough? Why should we create one more piece of content?

There were a lot of Holy Wars about education and all around it. Leaving them aside, I personally formulate the main purpose of education as follows:

```{admonition} The Fundamental Goal of Education
Create conditions allowing students to acquire knowldedge and skills at the desired level in the shortest possible period of time.
```

```{figure} https://slideplayer.com/7520891/24/images/slide_1.jpg
:align: center
```

Our attempt will technically rely on [Jupyter book](https://jupyterbook.org/en/stable/intro.html), an open-source tool for building publication-quality books and documents from computational material.

## Jupyter-book demo

To introduce the capabilities of Jupyter book along with some methodological ideas I wrote the [e_book](https://fedmug.github.io/e_book/intro.html). For now it consists only of one chapter devoted to the Euler number.

The main features:

- interactive quizzes (taken "as is" from [here](https://github.com/jmshea/jupyterquiz));
- mix of narrative and executable content as it is usually done via markdown and code cells in Jupyter notebook;
- pictures and visualizations (sometimes interactive);
- available online on any device.

Hopefully, during this course we'll write something similar about machine learning.

## Course assessment

| Activity             | Final scores |
| -------------------- | ------------ |
| Attendance           | $10\%$       |
| Practice             | $10\%$       |
| Midterm              | $10\%$       |
| Jupyter book project | $30\%$       |
| Final exam           | $40\%$       |

## Project team construction

Successive completion of the project requires effective team collaboration. The team should consist of several students with different roles:

- technical writer
- author of executable content
- designer of interactive plots
- designer of quizzes
- <strike>the most useless...</strike> project manager

The goal of every team is to create a nicely looking section in the ML book.

### Technical writer

- writes clear and neat [narrative content](https://jupyterbook.org/en/stable/content/index.html#) in Markdown
- looks for consistency with all other types of content
- translates some Russian texts into English if necessary

### Author of executable content

- writes [executable content](https://jupyterbook.org/en/stable/content/executable/index.html) in Jupyter notebook
- suggests ideas of python calculations and static plots which would enrich the narrative content
- searches for existing datasets and visualizations
- tries different models of machine learning

### Designer of interactive plots

- uses [plotly](https://plotly.com/python/) or [pywidgets](https://ipywidgets.readthedocs.io/en/stable/) or something else to create interactive visualizations
- searches for places where it would be quite beneficial to insert interactive elements
- suggests ideas of quizzes which could be solved by investigating of interactive content

### Designer of quizzes

- searches for ideas of single/multiple choice and numeric quizzes
- writes quizzes using [Jupyterquiz](https://github.com/jmshea/jupyterquiz) in a separate Jupyter notebook
- encodes the quiz bodies and inserts them into main content

### Project manager

- tracks the progress of each member of the team
- checks for consistency of all types of content, notations and cross-references to other parts of the book
- searches for different sources of information
- communicates with PMs of teams which work on related topics
- communicates with [BDFL](https://en.wikipedia.org/wiki/Benevolent_dictator_for_life)

## The main tool

```{figure} chatGPT.png
:align: center
```

## Tips

- Don't copypaste from chatGPT, it can serve just as a starting point
- Study carefully the documentation of [Jupyter book](https://jupyterbook.org/en/stable/intro.html) and [jupyterquiz](https://github.com/jmshea/jupyterquiz); pay special attention to the things relevant to your role in the team
- The Jupyter book ecosystem allows to produce diverse content, make advantage of this as much as you can (see [e_book](https://fedmug.github.io/e_book/intro.html) for a baseline)
- As a starting point, clone the [ML book repo](https://github.com/Fedmug/kbtu-ml-book) and check that you can build the book locally
- Clone only one branch of [ML book repo](https://github.com/Fedmug/kbtu-ml-book) which corresponds to your section:
  `git clone -b BRANCH_NAME --single-branch https://github.com/Fedmug/kbtu-ml-book.git BRANCH_NAME`
- Try to investigate all possible sources of information about your topic, especially those from [ML resources](./resources.md)
- Think about links between parts of your section or to some other sections and chapters
- Keep in mind that you are creating content for newbies
