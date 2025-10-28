# CodeBook  
*Pure Python Data Analysis & Recommendation System*

## Table of Contents  
- [About](#about)  
- [Features](#features)  
- [Getting Started](#getting-started)  
  - [Prerequisites](#prerequisites)  
  - [Installation](#installation)  
  - [Running the Notebooks](#running-the-notebooks)  
- [Project Structure](#project-structure)  
- [Usage](#usage)  
- [How It Works](#how-it-works)  
  - [Data Cleaning & Pre-processing](#data-cleaning--pre-processing)  
  - [“People You May Know” Recommendation](#people-you-may-know-recommendation)  
  - [“Pages You Might Like” Recommendation](#pages-you-might-like-recommendation)  
- [Contributing](#contributing)  
- [License](#license)  
- [Contact](#contact)

---

## About  
CodeBook is an end-to-end recommendation system built using **pure Python (no external libraries)**. It processes raw user-data, performs cleaning, analyses relationships, and generates two distinct recommendation features:

- **People You May Know**: Suggests potential connections based on mutual friends and network structure.  
- **Pages You Might Like**: Suggests pages (or items) a user may be interested in, by employing collaborative-filtering style logic on user-interest overlap.

The goal is to illustrate how you can build a recommendation engine from scratch, using fundamental Python structures and algorithms.

---

## Features  
- Clean and structure raw data: handle missing values, remove duplicates, standardise formats.  
- Relationship analysis: detect mutual friends and generate “people you may know” suggestions.  
- Interest-based recommendation: analyse user → page sheet, create similarity measures, recommend new pages.  
- Fully documented with Jupyter notebooks to explore each step interactively.

---

## Getting Started

### Prerequisites  
- Python 3.x installed on your system  
- Git (to clone the repo)  
- Familiarity with Jupyter Notebook (optional but helpful)

### Installation  
1. Clone the repository:  
   ```bash
   git clone https://github.com/shreyashsalwe23/CodeBook.git
   cd CodeBook

   ```

2. (Optional) Create a virtual environment:

   ```bash
   python3 -m venv venv
   source venv/bin/activate     # on Unix/Mac  
   venv\Scripts\activate        # on Windows  
   ```

### Running the Notebooks

Since the project uses Jupyter notebooks:

```bash
jupyter notebook
```

Then open and run:

* `01_introduction.ipynb` — Overview & setup
* `Data_cleaning.ipynb` — Data cleaning & preprocessing
* `people_you_may_know.ipynb` — People recommendation logic
* `pages_you_might_like.ipynb` — Page-recommendation logic

Feel free to explore, tweak, and extend.

---

## Project Structure

```
CodeBook/
├── 01_introduction.ipynb
├── Data_cleaning.ipynb
├── people_you_may_know.ipynb
├── pages_you_might_like.ipynb
├── data.json
├── data2.json
├── massive_data.json
└── README.md
```

* `*.ipynb` — Jupyter notebooks illustrating each major step
* `data*.json` — Sample datasets used in the workflow
* `README.md` — This file

---

## Usage

* Use the notebooks as a learning resource or as a template for your own recommendation system projects.
* Replace or extend the sample data with your real datasets.
* Add more features: e.g., weighting edges, introducing user-profile features, exploring other algorithms.
* Compare performance (though this version focuses more on conceptual clarity than large-scale optimisation).

---

## How It Works

### Data Cleaning & Pre-processing

* Load the JSON files, convert into manageable Python data structures
* Handle missing values and anomalies, remove duplicates
* Standardise formats so that downstream processing is clean and consistent

### “People You May Know” Recommendation

* Based on mutual friends: for each user, identify common friends with other users
* Suggest new connections by ranking potential friends by number of mutual connections

### “Pages You Might Like” Recommendation

* For each user, track what pages (or items) they liked/visited
* Build similarity between users (or between pages) based on overlapping interests
* Recommend pages the user hasn’t yet interacted with, but similar users have

---

## Contributing

Contributions are welcome! If you’d like to add features, fix bugs, or optimise the logic:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m "Add some feature"`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request describing your change

---

## License

This project is released under the [MIT License](LICENSE).
(Include the full license text in a `LICENSE` file if you haven’t already.)

---

## Contact

Created by **Shreyash Salwe** – feel free to reach out if you have questions or feedback!
GitHub: [shreyashsalwe23](https://github.com/shreyashsalwe23)

---

*Thanks for checking out CodeBook — happy exploring and coding!*

```

