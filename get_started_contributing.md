## Get Started Contributing
Hello new friend,

Thank you for being part of the Prophet community and on your contribution to its continued legacy. 
We compiled this page with practical instructions and further resources to help you get started.

Please come join us on our [Slack](http://neuralprophet.slack.com/), you can message any core dev there.

### Get Started On
We created a [project kanban](https://github.com/ourownstory/neural_prophet/projects/8) with all tasks where we would appreciate your help! 
They can be done somewhat in isolation from other tasks and will take a couple hours up to a week of work to complete.

### Dev Install
Before starting it's a good idea to first create and activate a new virtual environment:
```python
python3 -m venv <path-to-new-env>
source <path-to-new-env>/bin/activate
```
Now you can install neuralprophet:

```python
git clone <copied link from github>
cd neural_prophet
pip install -e ".[dev]"
neuralprophet_dev_setup
git config pull.ff only 
```
Notes: 
* Including the optional `-e` flag will install neuralprophet in "editable" mode, meaning that instead of copying the files into your virtual environment, a symlink will be created to the files where they are.
* The `neuralprophet_dev_setup` command runs the dev-setup script which installs appropriate git hooks for Black (pre-commit) and Unittests (pre-push).
* setting git to fast-forward only prevents accidental merges when using `git pull`.

### Style
We deploy Black, the uncompromising code formatter, so there is no need to worry about style. Beyond that, where reasonable, for example for docstrings, we follow the [Google Python Style Guide](http://google.github.io/styleguide/pyguide.html)

As for Git practices, please follow the steps described at [Swiss Cheese](https://github.com/ourownstory/swiss-cheese/blob/master/git_best_practices.md) for how to git-rebase-squash when working on a forked repo.
