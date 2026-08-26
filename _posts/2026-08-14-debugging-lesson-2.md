#  Course.Fast.AI Lesson 2

This is part of an initiative to document any errors, creations, etc. for various courses I pursue. Have found these to be very helpful based on past projects/roles. This is also just in case I completely fudge up changes and need to reference what I did in the past.

Below are some of the notes I took in the process of debugging during Course.Fast.AI's second lesson.

## Computer Setup via `/fastsetup`

### 1. Entering Linux Terminal...

Just type da `wsl` in da Powershell. Linux! 

### 2. Trouble running `setup-conda.sh` on Windows

When attempting computer setup using [this](https://github.com/AnswerDotAI/fastsetup) repo, running `./setup-conda-clean.sh` gave me the following error:
> env: $'bash\r': No such file or directory\
> env: use -[v]S to pass options in shebang lines

This is because `setup-conda.sh` typically has Unix-style instead of Windows-style endings. To fix this, you can either modify `setup-conda.sh` or if you are like me and are deathly afraid of fudging existing files up (as will likely happen), create a new file `setup-conda-clean.sh` and run it:
> tr -d '\r' < setup-conda.sh > setup-conda-clean.sh\
> chmod +x setup-conda-clean.sh\
> ./setup-conda-clean.sh

This should fix things.

## Running FastAI Kernel Locally via Jupyter

One critical step in order to complete 02 is being able to run Jupyter locally: specifically, run an `.ipynb` which then helps generate `app.py` to deploy our model. An issue I faced when doing this is when attempting to run:
> learn = load_learner('model.pkl')

I got an error ending in:
> Custom classes or functions exported with your 'Learner' not available in namespace. Re-declare/import before loading:
>   'Resolver' object has no attribute '_\_dict__'

The issue is that the kernel for your Jupyter notebook must be set to `Python 3.12 (fastai)`.  While simply changing the notebook's kernel to that version will work, in my case I did not see that option initially in the dropdown when attempting to change it. To resolve this, try creating and activating the `Python 3.12` environment via terminal first, registering the environment with Jupyter, and then refreshing/reopening Jupyter for which you should now see the option. To register, I ran:
> python -m ipykernel install --user --name fastai_py312 --display-name "Python 3.12 (fastai_py312)"

If this doesn't work, ask an AI model.

# Footnotes

[^1]: Astronomenal: astronomically phenomenal
