---
title: "Git (Version Control System)"
datePublished: Wed Sep 27 2023 10:42:06 GMT+0000 (Coordinated Universal Time)
cuid: cln1ma25w000v08mf3nl68xk3
slug: git-version-control-system

---

Lec - 11.   Introduction of Git 
=======================

Source Code Management:-

	1. Centralized Version Control System (CVCS)
	2. Distributed Version Control System (DVCS)
	
	• Centralized Version Control System (CVCS)
	
	
		Working Copy
	
	
	      
	           Working Copy                                                                        Repository
							
							
							
		Working Copy                                                                                                   

		
		
	• Distributed Version Control System (DVCS)
		○ Linux Torvalds
		
		
		                                                                                        Repository
		
		
											
											
										Push                  Pull
											
											
										
				Local Repo                                                  Local Repo                                                       Local Repo
				
				
				
			Commit                                                        Commit                                                           Commit
				
				
				
				Working Space                                          Working  Space                                                Working Space
				
				      PC-1                                                               PC-2                                                                     PC-3
		
		
		
		Git - Software
		GitHub - Service/Storage
		Gitlab -Service/Storage
		
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Lecture -12.  Stages of git and its Terminology
====================================

			Stages of git / workflow





					   Staging Area








				India EC 2                                                                                                                                                                                                                       London EC 2                                




						Working Directory      ---------> Add ---------->       Staging Area       --------> Commit -------->    Local Repo




Term :- 
	Repository	It is  a place where you have all your codes or kind of folder on server 
	Server	It stores all repositories
		It contains metadata
	Working Directory	Where you write the code ,modification and delete 
	
Advantages of Git:-
	• Free and Open Source
	• Fast and Small
	• Written in C language
	• Secure
	• No need Powerful Hardware
	• Easier Branching 

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Lecture -13.  How to use git and create GitHub account 
============================================















Command 
	Sudo su	Give the root permission 
	Yum update -y 	Update the machine 
	Yum install git -y 	Install git 
	Git --version	See the version
	Git config --global user.name "name"	Give user name 
	Git config --global user.email "test@gmail.com"	Give the email
	Git config --list	See the list 
	
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Lecture -14. How to commit , push and pull from GitHub
==============================================

Command:-
	Git init	initialize
	Git status	Check status
	Git add .	Save in staging area
	Git commit -m "message" 	Save in local repo
	Git status	Check status
	Git log 	Check log 
	Git show <commit id>	Check code by commit id
	Git remote add origin <centralgit url >	
	Git push -u origin <branch_name>	
	Enter user name and password
	Vi .gitignore	 commit is ignore of this extensions
	*.css
	*.text
	Git log --oneline	One line log
	Git log --oneline --grep "7"	Search specific message
	
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
	
Lecture -15. How to Create Branch , Merge and stash
============================================


Branch-1
	O---------O-------O
	|
	|
	O--------O-------------------O---------O
				    |
				    |
				    O-----------O--------O

	


	Branch :-
		○ This is Concept is Useful for Parallel Development.
		○ You can create any number of branches.
		○ Change are personal to that particular branch.
		○ Default Branch is "Master"
		○ Copy all data in branch from master branch.
	
	Command :-
		Git branch	Show branch list
		Git branch <branch1>	Create branch 
		Git checkout branch1	Switch to  branch1
		Git branch -d branch1	Delete the branch
		Git branch -D branch1	Forcefully delete 
		Git log --oneline	Show the log
			
		---------> Merge	
		Git merge <branch1>	Merge the branch1
		Git log --oneline	Show log in one line 
		Git push origin master	Push on the central repo 
			
		---------> conflict 	Edit file and remove the conflict
			
		---------> Stashing	
		Git stash	To stash on the item
		Git stash list	To see stashed item list
		Git stash apply stash{0}	To apply stashed item
		Git stash clear	Clear the stash item
			
		----------> Reset	
		Git reset <filename>	Remove from staging area
		Git reset .	Remove all Whatever in staging area 
		Git reset --hard	Before Commit Empty workspace and staging area
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
		
Lecture -16. How to do git revert, Tag and GitHub clone
==============================================
	
	Git revert :- The revert command helps you undo on existing commit.
			§ It does not delete data 
			§ Reverted to the previous stages
			§ Version control moves forward and your work is backward
			
		Command
			Git status	Check the status
			Cat > new file	Create new file
			Git add	Send to staging area
			Git commit -m "new commit"	Send to local repo
			Git log --oneline	Show log in one line 
			Git revert <commit id>	Undo the code 
				
			----------> Remove Untracked files	
			Git clean -n 	Ask before delete
			Git clean -f 	Forcefully
				
			----------> Tags	
			Git tag -a <tag_name> -m <message>	To apply tag
			Git tag	See the list of tag
			Git show <tag_name>	Show content
			Git tag -d <tag_name>	To delete a tag
				
			-----------> Git Clone	
			Git clone <Url>	Clone the repo
		
	
	

Auth token 	
	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

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

	Brief:-
		
		Question:
				² What is Git?
				² How many types of version control system?
				² What is Stand for CVCS and DVCS ?
				² What is CVCS and DVCS?
				² What is Different b/w git and Github?
				
				² What is Staging Area ?
				² What is commit ?
				² What is Repository?
				² What is working Directory ?
				² Advantages of Git ?
				 
				² What is Branch?
				² What is Default Branch?
				² What is stashing?
				² What is Git Revert?
				  
				
		Command 
			Sudo su	Give the root permission 
			Yum update -y 	Update the machine 
			Yum install git -y 	Install git 
			Git --version	See the version
			Git config --global user.name "name"	Give user name 
			Git config --global user.email "test@gmail.com"	Give the email
			Git config --list	See the list 
				
			------------------> Initialize	
			Git init	initialize
			Git status	Check status
			Git add .	Save in staging area
			Git commit -m "message" 	Save in local repo
			Git status	Check status
			Git log 	Check log 
			Git show <commit id>	Check code by commit id
			Git remote add origin <centralgit url >	
			Git remote set-url origin <url >	Set to our url 
			Git remote -v 	Check the set git url 
			Git push -u origin master	
			Enter user name and password
			Vi .gitignore	 commit is ignore of this extensions
			*.css
			*.text
			Git log --oneline	One line log
			Git log --oneline --grep "7"	Search specific message
				
			------------------> Branch	
			Git branch	Show branch list
			Git branch <branch1>	Create branch 
			Git checkout branch1	Switch to  branch1
			Git branch -d branch1	Delete the branch
			Git branch -D branch1	Forcefully delete 
			Git log --oneline	Show the log
				
			------------------> Merge	
			Git merge <branch1>	Merge the branch1
			Git log --oneline	Show log in one line 
			Git push origin master	Push on the central repo 
				
			------------------> conflict 	Edit file and remove the conflict
				
			------------------> Stashing	
			Git stash	To stash on the item
			Git stash list	To see stashed item list
			Git stash apply stash{0}	To apply stashed item
			Git stash clear	Clear the stash item
				
			------------------> Reset	
			Git reset <filename>	Remove from staging area
			Git reset .	Remove all Whatever in staging area 
			Git reset --hard	Before Commit Empty workspace and staging area
			Git status	Check the status
			Cat > new file	Create new file
			Git add	Send to staging area
			Git commit -m "new commit"	Send to local repo
			Git log --oneline	Show log in one line 
			Git revert <commit id>	Undo the code 
				
			------------------> Remove Untracked files	
			Git clean -n 	Ask before delete
			Git clean -f 	Forcefully
				
			------------------> Tags	
			Git tag -a <tag_name> -m <message>	To apply tag
			Git tag	See the list of tag
			Git show <tag_name>	Show content
			Git tag -d <tag_name>	To delete a tag
				
			------------------> Git Clone	
			Git clone <Url>	Clone the repo
