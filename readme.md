##Working area	Index		Repository
##Lokalt	efter add	efter commit

git checkout *branch* (�ndrar Working area, Index och Repository)

--L�gga till filer--
git add *fil* (Working area -> Index)
git commit *fil* (Index -> Repository)

--Ta bort filer--
git rm (Tar bort filer fr�n Index OCH Working area)
git rm *fil* --cached (Tar enbart bort filer fr�n Index aka motsatsen till git add)


--Se skillnad--
git diff *fil* (Skillanden mellan working area och index)
git diff *fil* --cached (Skillnaden mellan index och repository)
git diff branch1 branch2 (Skillnaden mellan branches)

--Flytta fil--
git mv *fil* *nyfil* (Om man vill �ndra filnamn eller plats inkl. add med f�r�ndringen)

--Flytta HEAD (Dvs current branch, HEAD pekar p� en branch som pekar p� en commit)--
git reset HEAD --hard *commit* Flyttar HEAD i Repository till Index och Working Area)
git reset HEAD --mixed *commit* Flyttar HEAD i Repository till Index) *Default*
git reset HEAD --soft *commit* (Flyttar HEAD i Repository och enbart d�r)
git reset HEAD --arg^ (Flyttar fr�n HEAD i Repository fr�n senaste commit till det man vill med args fr�n ovan)
git reset HEAD *fil* --mixed (Unstagear specifika filer i Repository till Index. --hard fungerar inte)
git checkout HEAD *fil* (Flyttar fil fr�n Repository till Index och Working area)

--Stash/Spara utan att commita--
git stash --include-untracked (Flyttar fr�n index och working area till stash samt updaterar Working area och Index fr�n Repository)
git stash list (Lista utav alla stash, info fr�n senaste commit)
git stash apply (Updaterar index och working area med det fr�n stash) *default f�rsta i listan anv�nd annars nummer*
git stash clear (Tar bort allt ifr�n stashen)

--Konflikter--
<<<<<<< HEAD
Onion
========
Tomato
<<<<<< Tomato

Tomato branchen har en info om en rad och HEAD en. V�lj det som �r det korrekt och sudda ut det andra.
git add *fil* , git commit -m "konflikt" (H�r betyder git add att du l�st konflikten)





