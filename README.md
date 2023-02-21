# Information
This is a minimal example to host a [FastAPI](https://fastapi.tiangolo.com/) app on [Deta Space](https://deta.spaace).

Reference: https://deta.space/docs

# Running

Official Guide: https://deta.space/docs/en/introduction/first-app

Alternatively, you can use [Google Cloud Shell](https://shell.cloud.google.com) if [Space CLI](https://deta.space/docs/en/basics/cli) doesn't work on your PC.

1. Login to [Google Cloud Shell](https://shell.cloud.google.com) (requires [Gmail](http://mail.google.com) account).
2. Select the default starter project or create a new one.
3. Run `curl -fsSL https://get.deta.dev/space-cli.sh | sh` in Terminal to install Space CLI.
4. Run `space login` and enter your access token when prompted.
    - Access Tokens can be generated from https://deta.space -> Settings.
5. Run `space new` and enter your app name, which links your project to your space app and generates a `Spacefile`.
6. Copy paste `main.py` and `requirements.txt` to your project, and overwrite `Spacefile` with this repo's `Spacefile`.
    - This repo's `Spacefile` defines a micro with all routes being public.
7. Run `space push` to upload the files to Deta Space.
8. Go to https://deta.space and click on your app to run it.
    - This opens a URL that looks like this `https://{app_name}-1-a1234567.deta.space`.
    - Custom domains are available and custom subdomains are coming in the future.
    
# Limits
Micros have a timeout limit of 10 seconds = you only have 10 seconds to process a request. 

There were other limits but they were removed/no need to worry about: https://deta.space/limits
