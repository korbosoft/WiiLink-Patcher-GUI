# Translating WiiLink Patcher

To translate the patcher, you'll need some things installed on your PC first:
- [Qt OSS SDK](https://www.qt.io/download-qt-installer-oss) (make sure to install Qt Linguist 6)
- [Git](https://git-scm.org)
- [Python](https://python.org)

### Step 1: Forking and cloning the repository
First, you'll want to fork, clone and enter this repository.

Follow [this link](https://github.com/WiiLink24/WiiLink-Patcher-GUI/fork) to fork the repo to your GitHub account, then run the following commands to clone and enter your fork:
```
# If you named your fork something other than WiiLink-Patcher-GUI, make sure to swap out the repository name in these commands.

git clone https://github.com/<your username>/WiiLink-Patcher-GUI
cd WiiLink-Patcher-GUI/
```
After this, create a venv and activate it:
```
python -m venv .venv

# Windows
.venv\Scripts\activate

# macOS, Linux and other OSes
source .venv/bin/activate
```
Now, you can install the dependencies for the patcher:
```
pip install --upgrade -r requirements.txt
```

### Step 2: Adding your language
If your language does not already exist in the patcher, open `pyproject.toml` in a text editor, and copy and paste the sample language line into the `files` list, remembering to swap `XX` for your language's two-letter code.

### Step 3: Updating translation files
Run the following command to update all translation files, ensuring all the latest strings are present for you to translate:
```
python update_translations.py
```

### Step 4: Translating
Launch Qt Linguist, navigate to the `.ts` file for your language in the `translations` folder, and translate the strings!

### Step 5: Pushing
Finally, commit and push your changes to your fork. Then, open a pull request in this repository to add your language!