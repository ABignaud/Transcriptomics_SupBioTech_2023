---
layout: default
permalink: /Introduction/Config/
---

---
# Config

## Install docker-desktop

Downloads the executable
https://www.docker.com/products/docker-desktop/

![docker_desktop](assets/docker_desktop.png)

### To install it on Mac:
https://docs.docker.com/desktop/install/mac-install/

### To install it on Windows:
https://docs.docker.com/desktop/install/windows-install/

For Windows, you will probably encounter an issue with WSL at the end of the
installation. Here are the instructions to install it:

https://learn.microsoft.com/en-us/windows/wsl/install 

### To install it on Linux/
https://docs.docker.com/desktop/install/linux-install/


## Install the docker image

A `docker` image is an image of a computer with some software installed on it. 
Basically, by pulling and running the image you will locally install that 
computer on your computer and all of you will work exactly on the same machine.

To install go the search bar at the top and search for 
`abignaud/transcriptomics_supbiotech_2023`, search for an `image` and then pull
it. It will take a little time to download (few GB as there are the whole OS for
the computer). If you don't find the image, try to search just `abignaud` or 
with only the part of the name.

![download_image](assets/image_download.png)

## Run the docker image

Create a `directory` where you want to store the files for the analysis.
Download the archive file in that directory (the link is in the email you 
received). 

Then go the image stuff. You should have a new image.

Run it and use the advanced settings:
- Select a name for the container (Transcriptomics_SupBioTech_2023 for example)
- Select the `directory` you created earlier as a host path
- Choose `/data/` as container path.

![setting_container](assets/setting_container.png)

## Open terminal

Do not do this part if it's not working.

Now open the terminal (3rd panel). If you didn't manage to do that step, it's 
ok.

For some reason, it seems that you may have to leave the mounted repository to 
be able to assess the files in it. To do that enter these commands.

```sh
cd ..
cd data
ls 
```

The `ls` should yield you the list of the files inside your folder. So the
archive that you previously downloaded should be listed. If not, it's not 
working. Check that you have loaded the right folder in the advanced settings 
used.

Open the archive file, by entering that command:

`tar -xvzf transcriptomics_supbiotech_2023.tar.gz`

Congratulations your environment is set up !


## Install IGV 

For the Session 2,
[Integrative Genomics Viewer (IGV)](https://software.broadinstitute.org/software/igv/) 
will be needed. To isntall it go to the following page to download the 
executable and run it:

https://software.broadinstitute.org/software/igv/download
