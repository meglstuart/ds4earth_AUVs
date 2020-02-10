# Hi Patrick!
I'm going to post general friendly comments on stuff you upload to github here. You can respond to things within the document if you want.
> perhaps you can respond to things like this?

## General stuff
- I removed the spaces from the names of folders and files that you uploaded. When coding or using the terminal to navigate around directories, spaces have to be escaped using '\ ' which can get kinda annoying. I've heard people refer to file names with spaces in them as 'rude'. I don't know if I'd go that far, but I certainly prefer not using them.

- Make sure that when you upload code to the repo it runs out-of-the-box. That usually just means that variables are properly named and initialized, and that when you import data from files, you have the proper path. i.e. 'glider_path_csvs/ram1.csv' instead of 'ram1.csv'. The best way to do this is to keep your local version of the repository clean, meaning that you don't have a bunch of extra files that aren't in the repo, and before committing a jupyter notebook, restart the kernel (looks like a reload button at the top of the jupyter lab editing pane) and run the entire notebook (can be done with the dropdown menu at the top labeled 'Run')

## pelagia_path and rameses_path notebooks
- These look really nice. Excellent commenting.  
- This is just my opinion: I prefer to not have large data tables print by default, but it's nice to have optional print statements for debugging, so I leave the print statements useful for debugging in the code, but comment them out or use something like
  ``` python
  verbose = False
  if verbose:
    print(stuff)
  ```
- What do you think about the odd outlier points? Is it possible that it is some weird mistake when converting from .dat to .csv files? What is the data like around them? Do they occur after a long break in communication meaning that it's possible that the points might actually be accurate glider locations? Or do the occur very close to nearby points, meaning that they are actually extraneous data and can be safely removed? Can you check into this and report back.
- Lastly, and this is a very important one. When you download data, convert, and post it to the repo, please make a text file in the data folder with the exact url where you fetched each data file, and a quick description of what is in each. For the current data, this could be something like
```
All files in this folder consist of positional data sent from the
respective glider at each surfacing event in the mission. The data
comes from a .dat file from the LBWB site which I converted to csv
format.
ram1.csv - Ramses mission 1 of 5. Dec 14, 2011 - Jan 5, 2012
[url]
ram2.csv - ...
[url]
etc.
```
