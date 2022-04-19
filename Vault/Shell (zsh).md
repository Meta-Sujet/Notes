- in computing,shell is a computer program whichexposes an operating system's services to a human user or other programs.In general, operating system shells use either a command-line interface or graphical user interface., depending on a computer's role and particular operation.
-your interface to the operating system.
-enables the user to interact with computer.
-shell is the outermost layer of the operating system,shells incorporate a programming language to control processes and files, as well as to start & controlother programs.

Computer ----------------->Shell <------------------Human
	
```
Graphical User Interface           Command Line Interface
		 (GUI)                            (CLI)

- User friendly                    - Time saving
- Easy to explore                  - More posibilities
```

Mac Terminology:
```dart
       Terminal                         Shell
Text Input Environment            Text Input Interface
     ('Hardware')                    ('Software')
     
									 Bash-shell   X 
|ooo---user-zsh------|           <---zsh(z-shell) √ <- using this 
|--------------------|
|.....               |
|........            |
|                    |
|____________________|													     
```


- 3 core directories: 
```dart
/         Macintosh Hd - Root folder / directory 
/Users    Users - directory
~         Home - directory 
```

- customize zsh: 
code ~/.zshrc
code ~/.p10k.zsh
p10k configure

- pwd - print working directory
- ls - list items
- ls -a  - show hidden fails
to create hidden files in folders use dot before file name:   .index.html
command + shift + .  - show/hide hidden files in folder
- ls -l  -(L) more info about files
- ls | grep file/foldername
- clear
- command + k  -clear code
- cd  -change directory
- cd /  -navigate to Root directory
- cd ~  -navigate to Home directory
- cd /Users  -navigate to Users directory with absolute path
- cd desk..   -use Tab for auto-cpmplete
- cd .. - უკან გამოსვლა, ერთი საფეხურით ზემოთ ფოლდერში(იერარქიულად)
- cd ../../Applications  - ორი ფოლდერით უკან გამოსვლა და შემდეგ Applications-ფოლდერში შევლა
- use up&down arrow to see previous commands
- touch index.html  -  ფაილის შექმნა
- touch scrpit.js style.css. -რამდენიმე ფაილის ერთად შექმნა
- touch foldername/index.html
- mkdir folder  -ფოლდერის შექმნა
- mkdir folder1 folder2
- mkdir test/web-dev
- mkdir web\ dev  -ფოლდერის სახელი space-ით
- cd web\ dev
- rm index.html  -ნაგვის ურნაში არ ვარდება,ვეღარ დავაბრუნებთ rm-თი წაშლილს
- rm style.css script.js  
- rmdir folder1   -თუ ფოლდერში არის ფაილები ამ გზით ვერ წავშლით
- rmdir folder1 folder2
- rm -r folder1 -თუ შიგნით ფაილებია ვშლით ამ გზით
- man rm  - manual
- man ls -და ასე შემდეგ
- desktop % cp web-dev/index.html ./            - ./ copy in this folder(desktop)
- cp -r web-dev ~  -copy in Home directory
- mv test.txt folder1  -cut
- folderN % mv test.txt ../  -უკან გამოსვლა და იმ ადგილას ჩასმა
- mv ../web-dev web-dev
- mv index.html index2.html - rename
- open . 
- open folder
- open index.html
- open -a safari - გახსენი აპლიკაცია
- code file.html  - ფაილს გახსნის vscode-ში 
- nano test.txt  - ტექსტის შეცვლა/დამატება ტერმინალიდან
- cat test.txt - see whats written inside in terminal
- less test.txt
- cat index.html | grep blabla
- history
- sw-vers -software version
- say hello ...
- say -v "?"
- say -v Milena hello
- du -hs folder - folder size
- unzip filename
- flutter create foldername