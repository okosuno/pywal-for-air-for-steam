# disclaimer
#### this thing is kind of busted right now. i haven't had time to comb through air for steam to get a 100% handle on the theme options. do not use this unless you plan on messing around with the template.

## pywal for air for steam (for now)

__[air for steam](https://github.com/airforsteam/Air-for-Steam)__ is a now abandoned theme project for steam which i liked.  

__[pywal](https://github.com/dylanaraps/pywal)__ is a system theme uniformity project which is still supported that i _very much_ like. 

i've been spurred into action by my dissatisfaction with current pywal-steam theming solutions, particularly because pywal's templating system doesn't support the kinds of RGB codes steam likes.  

if you don't have experience with what using deprecated steam skins looks like, you should know that this is only going to be a comprehensive skin solution for Steam's "Small Mode" display. in the discussion section i talk about how i will do the bigger project of smooshing pywal and a current steam skin together later.

## requirements

you need a current python probably  
__[pywal](https://github.com/dylanaraps/pywal)__, or the fork i use: __[pywal-16-color](https://github.com/sonjiku/pywal)__   
__[air for steam](https://github.com/airforsteam/Air-for-Steam)__ - if you don't have the skin installed __first__, this script will not work  

if you use arch, all of these can be found in the AUR

## install

clone the repo to somewhere tidy where you can reference it later:  
`git clone https://github.com/okosuno/pywal-for-air-for-steam.git`  
get in there:  
`cd pywal-for-air-for-steam`  
intall requirements:  
`pip install -r requirements.txt`  

## execution

run script without flags to start:  
`python pywal_air.py`  
`--help` to get help.  
`--template` to refresh the template.  
`--config` to perform setup again.  

## what does it do exactly

1. creates a folder and config file for itself in your `.config` folder. 
2. prompts you for the location of some file/dir locations. 
3. moves its template file into your template folder.  
4. refreshes pywal.  
5. creates a symlink of the cached pywal output of that file to where __air for steam__ keeps its theme files.  
6. modifies __air for steam__'s `config.ini` to accomodate the changes.

you can tweak values inside the template file to your hearts content and run `python pywal_air.py --template` to push the updated modifications down the pipeline. 

## troubleshooting

at this stage, i've barely tested it, it's probably busted. i am not very good at this so if its busted please tell me how to fix it. thanks.

## discussion

i don't write a lot of code and i am hastily uploading this after working on it for a few hours and will come back to it later. presently i'm using __air for steam__ because i really only use steam in its 'small mode' form. so i don't really see all the jank behind the curtain.

that being said, i am looking at __[Pure](https://github.com/Snudgee/Pure)__, which is beautiful and well-supported. it uses __[SFP](https://github.com/PhantomGamers/SFP#sfp-formerly-steamfriendspatcher)__ to ensure that it modifies the friends list and library appearance. so i think when i come back to this i will take a look at switching to that.
