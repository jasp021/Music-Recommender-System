# Music Recommender System using Decision Tree

(https://www.python.org/)
(https://scikit-learn.org/stable/)
(https://graphviz.org/) 
(https://joblib.readthedocs.io/en/latest/)
(https://learn.microsoft.com/en-us/windows/wsl/)
(https://jupyter.org/try)
(https://opensource.org/licenses/MIT)

## Source

The initial learning for this project was derived from the following video:

[Video Link](https://youtu.be/7eh4d6sabA0?si=JuLwpAN-0vYhXk-4)

## Description

This project demonstrates the creation and visualization of a decision tree for a music recommender system. The decision tree is built using the `scikit-learn` library in Python, considering features like 'age' and 'gender' to predict music preferences. The project also includes detailed steps to visualize the decision tree as a PNG image, including troubleshooting common issues encountered during the process.

This project was developed using Python within a WSL2 Ubuntu environment and Jupyter Lab.

## Technologies Used

-   **Python:** The primary programming language used for the project.
-   **scikit-learn (sklearn):** A powerful Python library for machine learning, used here for creating and exporting the decision tree.
-   **Graphviz:** An open-source graph visualization software used to render the decision tree into a graphical format.
-   **joblib:** A set of tools to provide lightweight pipelining in Python. Used here for installation purposes.
-   **WSL2 (Windows Subsystem for Linux 2):** The environment where the project was developed, specifically using Ubuntu.
    
-   **Jupyter Lab:** An interactive web-based development environment used for writing and running the Python code.

## Getting Started

To run this project and generate the decision tree visualization, follow the steps below:

### Prerequisites

-   **Python 3.x** installed on your system.
-   **pip** (Python package installer) installed.
-   **WSL2** with **Ubuntu** (if you want to replicate the exact development environment).
-   **Jupyter Lab** installed (if you want to run the code in a Jupyter Notebook).

### Installation

1.  **Clone the repository:**
    
    Bash
    
    ```
    git clone [https://github.com/jaspreetsk/Music-Recommender-System-using-Decision-Tree.git](https://github.com/jaspreetsk/Music-Recommender-System-using-Decision-Tree.git)
    cd Music-Recommender-System-using-Decision-Tree
    
    ```
    
2.  **Install necessary Python libraries:**
    
    Bash
    
    ```
    pip install scikit-learn joblib
    
    ```
    

### Running the Code

The core logic for creating and exporting the decision tree is likely within a Python script or a Jupyter Notebook. Assuming you have a Jupyter Notebook (e.g., `music_recommender.ipynb`), you can run it using the following command in your terminal:

Bash

```
jupyter lab

```

This will open Jupyter Lab in your web browser, where you can navigate to and execute your notebook. The provided Python code snippet should be present in one of the cells:

Python

```
from sklearn import tree

# Assuming 'model' is your trained decision tree model and 'y' is your target variable
tree.export_graphviz(model,
                    out_file='music-recommender.dot',
                    feature_names=['age', 'gender'],
                    class_names=sorted(y.unique()),
                    label='all',
                    rounded=True,
                    filled=True)

import joblib
# joblib is installed separately, no direct usage in this snippet but was needed for installation.

```

## Decision Tree Visualization

The `tree.export_graphviz` function will generate a `music-recommender.dot` file in your project directory. To convert this `.dot` file into a visual PNG image, you need to use Graphviz.

### Generating the PNG Image

Follow these steps to generate the `graph.png` file:

1.  **Install Graphviz:** If you encounter an error related to the `dot` command not being found, you need to install Graphviz on your Ubuntu system within WSL2. Open your Ubuntu terminal and run the following commands:
    
```
sudo apt update
```
```
sudo apt install graphviz 
```

3.  **Navigate to the project directory** in your Ubuntu terminal.
    
5.  **Execute the `dot` command:** This command will take the `music-recommender.dot` file as input and output a `graph.png` file.
    
    Bash
    
    ```
    dot -Tpng music-recommender.dot -o graph.png
    
    ```
    
    This will create a `graph.png` file in your project directory, showcasing the decision tree in a graphical format.
    

### Troubleshooting

During the process, you might encounter the following issues:

#### Issue: `'dot' command not found`

This error indicates that the Graphviz software is not installed or not in your system's PATH. The solution is to install Graphviz using the commands mentioned above in the "Generating the PNG Image" section.

#### Issue: `'joblib' not found in scikit-learn`

While `joblib` is not directly a submodule of `sklearn`, it's often used in conjunction with it for saving and loading models. If you encountered an error suggesting that `joblib` needs to be installed separately, you have already resolved it by using `pip install joblib`. This ensures that the `joblib` package is available in your Python environment.



## License

This project is licensed under the MIT License.

```
MIT License

Copyright (c) 2025 Jaspreet Singh Kalsi

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

```

----------

Thank you for checking out this project! If you have any questions or suggestions, feel free to open an issue or submit a pull request.

---

