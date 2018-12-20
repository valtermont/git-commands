![](https://raw.githubusercontent.com/valtermont/git-commands/master/image.png)

git chery-pick - ты забираешь комиты из одной ветки в другую, это бывает полезно когда изменения сделаные другим разработчиком в его ветке, прямо сейчас нужны тебе в твоей ветке, и что бы не писать этот код заново, ты забираешь его комит себе в ветку

git rebase master - ты синхронизируешься с главной веткой в которую коммитят все разработчики проекта, это полезно когда кто-то изменил участок кода с которым ты сейчас работаешь в своей ветке, дабы через неделю ты смог без проблем смержиться с master веткой. Обычно делается каждое утро перед началом рабочего дня и в конце когда фича готова.

git merge - обычно используется когда у вас 2 и более master ветки (к примеру master и prototype) в этих ветках очень много комитов (и rebase здесь не подходит) и обчно через пару недель, maintainer репозитория наработки из prototype ветки "сливает" в master ветку по средствам этого самого git merge

P.S. Что бы легче предствить разницу между git merge и git rebase. Представь что merge как собачка на молнии у одежды - "сшивает" комиты по дате их создания.
В то время как git rebase как пожарная лестница - при применении твои коммиты крепится на конец родительской ветки

git merge используйте для мержа фич и фиксов в master ветку (как и делает это Github)
а git rebase используется для своей ветку в которой вы работаете над фичей что бы забрать последние изменения с master ветку (для этого есть очень удобная команда `git pull --rebase origin master`, аналог 3х команд (`git checkout master; git pull origin master; git checkout mybrach; git rebase master`)
