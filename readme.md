Working area	Index		Repository
Lokalt		efter add	efter commit

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
git reset --hard *commit* Flyttar HEAD i Repository till Index och Working Area)
git reset --mixed *commit* Flyttar HEAD i Repository till Index) *Default*
git reset --soft *commit* (Flyttar HEAD i Repository och enbart där)

