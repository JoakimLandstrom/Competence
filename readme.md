1. Working area | 2. Index | 3. Repository  
1. Lokalt | 2. efter add | 3. efter commit

git checkout *branch* (Ändrar Working area, Index och Repository)

--Lägga till filer--  
git add *fil* (Working area -> Index)
git commit *fil* (Index -> Repository)


--Ta bort filer--  
git rm (Tar bort filer från Index OCH Working area)
git rm *fil* --cached (Tar enbart bort filer från Index aka motsatsen till git add)


--Se skillnad--  
git diff *fil* (Skillanden mellan working area och index)
git diff *fil* --cached (Skillnaden mellan index och repository)
git diff branch1 branch2 (Skillnaden mellan branches)


--Flytta fil--  
git mv *fil* *nyfil* (Om man vill ändra filnamn eller plats inkl. add med förändringen)


--Flytta HEAD (Dvs current branch, HEAD pekar på en branch som pekar på en commit)--  
git reset HEAD --hard *commit* Flyttar HEAD i Repository till Index och Working Area)
git reset HEAD --mixed *commit* Flyttar HEAD i Repository till Index) *Default*
git reset HEAD --soft *commit* (Flyttar HEAD i Repository och enbart där)
git reset HEAD --arg^ (Flyttar från HEAD i Repository från senaste commit till det man vill med args från ovan)
git reset HEAD *fil* --mixed (Unstagear specifika filer i Repository till Index. --hard fungerar inte)
git checkout HEAD *fil* (Flyttar fil från Repository till Index och Working area)


--Stash/Spara utan att commita--  
git stash --include-untracked (Flyttar från index och working area till stash samt updaterar Working area och Index från Repository)
git stash list (Lista utav alla stash, info från senaste commit)
git stash apply (Updaterar index och working area med det från stash) *default första i listan använd annars nummer*
git stash clear (Tar bort allt ifrån stashen)


--Konflikter--  
git add *fil* , git commit -m "konflikt" (Här betyder git add att du löst konflikten)

--Historik--  
git log (--graph --decorate --oneline, --patch = detaljerad per commit, --grep *ord* = enbart see commits med ordet, -G*ord* = la till eller tog bort detta ord, -3 se de senaste 3 commitsen)
git log branch1..branch2 --online (Lista alla commits som är i branch2 men inte i branch1, dvs dessa skulle komma med vid en merge)
git show (detaljerad info om en commit, args = commit hash, eller en branch för att se en senaste commit, HEAD^ -> parent commit, HEAD ^^ parent parent alt HEAD~2)
git blame *fil* (Se vem som ändrat i en fil och när)
git diff HEAD HEAD^2 (Se vad som ändrats mellan två commits)

--Ändra historik--  
git commit --amend (Lägger till nya saker från Index till Repository, kopierar senaste commiten i HEAD också till den nya commiten och gör en ny commit, dvs lägger till nya saker till senaste commiten)









