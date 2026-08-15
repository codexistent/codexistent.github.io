#  A Book Rec, Among Other Stuff

## A Book Rec

Who are we? Where are we from? What are we here for? What are we made of? What are we? What is time? What is the purpose of life? What is outside of the universe? Is the universe finite? ~~Why am I sounding like Georgey Pig?~~

Do you ever sit down beneath the night sky, and wonder no matter how distant another person may be in the world, how they are still comfortably covered by the same twinkling darkness? It is beautiful and humbling at the same time, like being shrank in the best way possible. 

A Brief History of Time by Stephen Hawking is astronomenal[^1]. I have never read another nonfiction book that reads more like fiction. While I am sounding like all the thousands of book reviews online about this book, it is truly one that was and is so difficult to put down. I read it some years ago, but it being so memorable, started to re-read it earlier this week and it has been just as delightful. Ofcourse, there is no way to answer all the questions I have placed in the first paragraph, but this book shares more background, some context here and there; and questions those same unanswerable questions *with* or *alongside* you. There is some comfort in that.

## C.F.AI - 02

For context: part of an initiative to document any errors, creations, etc. for various courses I persue. Have found these to be very helpful based on past projects/roles. This is also just in case I completely fudge up changes and need to reference what I did in the past.

### Computer Setup via `/fastsetup`

#### 1. Entering Linux Terminal...

Just type da `wsl` in da Powershell. Linux! 

#### 2. Trouble running `setup-conda.sh` on Windows

When attempting computer setup using [this](https://github.com/AnswerDotAI/fastsetup) repo, running `./setup-conda-clean.sh` gave me the following error:
> env: $'bash\r': No such file or directory\
> env: use -[v]S to pass options in shebang lines

This is because `setup-conda.sh` typically has Unix-style instead of Windows-style endings. To fix this, you can either modify `setup-conda.sh` or if you are like me and are deathly afraid of fudging existing files up (as will likely happen), create a new file `setup-conda-clean.sh` and run it:
> tr -d '\r' < setup-conda.sh > setup-conda-clean.sh\
> chmod +x setup-conda-clean.sh\
> ./setup-conda-clean.sh

This should fix things.

## Footnotes

[^1]: Astronomenal: astronomically phenomenal
