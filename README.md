# GameDev-CheatingScenarios
This repo will be full of multiple projects that have cheat vs anti cheat scenarios.</br>
We will cover Battleye, Easy Anti Cheat, EQU8, FairFight, VAC, and many more ways cheat developers circumvent these anti cheats.</br>
I will show you things that you should not do if you care about your community.</br>

# Usermode vs Kernelmode
What is usermode? well its kinda simple actually.</br>
## Usermode
-usermode is an access level that a program has on your computer.</br>
-we are in usermode right now you are too discord is, VAC is and many other things are too.</br>
-it is the standard access level for all programs that dont need "special privleges".</br>
-A fancier way of saying usermode is ring 3 and this will be said multiple times throughout this project.</br>
-if something goes wrong in your usermode application it will just crash the application but your operating system will free the memory and cleanup after itself.</br>
-usermode anti cheats can only look down in usermode they cant look up into the kernel</br>
## Kernelmode
-kernel mode is an access level that your operating system has on your computer.</br>
-kernel mode is a special access level that has a lot of hoops to jump through on windows at least.</br>
-kernel mode is an access level that allows you to directly communicate with your operating system and hardware.</br>
-A fancier way of saying kernelmode is ring 0 and this will be said multiple times throughout this project.</br>
-if something goes wrong in your kernel driver your entire operating system will crash and the memory will not be cleaned up until you reboot your computer.</br>
-kernelmode anti cheats can look up and down in the kernel and see anything above it or below it(usermode)</br>
# Benefits of each
## Usermode Anti Cheat
**PROS**</br>
-Incredibly easy to make and if there is problems they are much easier to solve</br> 
-Good for quick little checks</br>
-Great with a Kernel Driver partnership(ioctl)</br>
-Good if your game is single player and your just preventing piracy</br>
-Best of all its absolutely amazing if your on a budget for an anticheat</br>
-Very easy to setup</br>

**CONS**</br>
-These can simply be bypassed sherely just by making a cheat run in ring0
-Cheats are not at all hard to make with usermode anti cheats since you have a million ways to do so</br>
  -Some including</br>
  -Internal Cheats done by injecting a dll into the game</br>
  -External Cheats done by opening a process handle into the game</br>
  -Kernel Driver Cheats done by making a kernel driver that is quite literally above the anti cheat </br>
-The Anti Cheating measures cant be as strong as a Kernel Anti Cheat could be</br>
-A Kernel Cheat can literally block attempts to prevent cheating
-Usermode cant load with the operating system like a kernel driver **COULD** (*props to riot games for actually changing the anti cheat industry and taking a step forward*)</br>

## Kernelmode Anti Cheat
**PROS**</br>
-Ridiculously powerful preventitive measures can be made</br>
-You can literally block certain functions from working</br>
-You can flat out block process creation of certain things</br>
-You can restrict the memory access potential on an application</br>
-You can look anywhere in memory the kernel table, page files what ever you want</br>
-You have infinite potential paired with a usermode anti cheat module for ioctl</br>
-You have direct hardware access
