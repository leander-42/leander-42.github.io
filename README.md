# Welcome

My name is Leander Rankwiler. I'm a Master's student in data science at BFH in Bern, Switzerland. Currently, I am dedicating my efforts to writing my master thesis titled **"Evaluating Bias in German and Dutch NLP Models"**. This work is conducted under the supervision of [Prof. Dr. Mascha Kurpicz-Briki](https://www.bfh.ch/de/ueber-die-bfh/personen/diqa4uibb7gl/).

The thesis is part of the broader [European Research Project on Biases in AI](https://www.biasproject.eu/), which aims to uncover and mitigate the inherent biases that exist within current language models. A part of my thesis was accepted at SwissText2024, see preprint [here](https://www.swisstext.org/programme/). The code is published on [github](https://github.com/BFH-AMI/BIAS) and a meta description of the code can be found on [arxiv](https://arxiv.org/abs/2407.18689).

I will graduate in Summer 2024 and am looking for opportunities starting Fall 2024.

[Google scholar](https://scholar.google.com/citations?user=8ixNAFkAAAAJ&hl=de&oi=ao)  
[Linkedin](https://www.linkedin.com/in/leander-rankwiler-4a0a2a89)  
Email: My last name at gmail  

## Work With Me
Let's connect on [Focusmate](https://www.focusmate.com/i/8fGk3BDo9x).

## Anonymous Feedback
I am always eager to get feedback of any kind. Feel free to share your thoughts through this [anonymous feedback form](https://docs.google.com/forms/d/e/1FAIpQLSc5kHGNz3s1VpJfUNnJ5CHcFFq6nr33OubTdO8i8GY-7YBnnA/viewform?usp=sf_link).

## Quotes I agree with
- "You learn nothing from life if you think you are right all the time." - Unknown
- "The real problem of humanity is the following: we have paleolithic emotions, medieval institutions, and god-like technology." - Edward Osborne Wilson

## My beloved AutoHotkey script
For windows.  
- Edit text and code **without lifting your hand** to the arrow keys or the mouse
- Move windows across screens
- Works system-wide
- You need [autohotkey](https://www.autohotkey.com/)
- (overrides shortcut win+I (settings) and win+K (connect devices)

```
#NoEnv  ; Recommended for performance and compatibility with future AutoHotkey releases.
; #Warn  ; Enable warnings to assist with detecting common errors.
SendMode Input  ; Recommended for new scripts due to its superior speed and reliability.
SetWorkingDir %A_ScriptDir%  ; Ensures a consistent starting directory.

;navigation, del, backspace
;the following lets you:
; -navigate with Alt + I,J,K,L
; -delete with Alt + O (whole word if you add Ctrl)
; -backspace with Alt + U (whole word if you add Ctrl)

!j::
Send {Left}
return

!l::
Send {Right}
return

!i::SendPlay {up}
return

!k::
SendPlay {Down}
return

!u::
Send {BS}
return

!o::
Send {Del}
return

!^u::
Send, ^{BS}
return

!^o::
SendPlay ^{Del} ;overrides the windows outline view shortcut
return


; the following lets you
; -navigation one word with Alt + Ctrl + J,L
; -jump 5 lines with Alt + Ctrl + I,K
; -jump to the end/start of the line with: Alt + H,ö

!^j::
Send ^{Left}
return

!^l::
Send ^{Right}
return

;navigation down/up 5 lines at a time
!^i::
Send {up 5}
return

!^k::
Send {down 5}
return

!ö::
Send {End}
return

!h::
Send {Home}
return


;the following lets you
; -mark words (right/left) with Alt + Shift + J,L
; -mark text up/down (also usable to mark whole line): Alt + Shift + I,K
; -mark whole text to start/end: Alt + Shift + H,ö
; -alternative escape: Alt + N

;mark text to the right
!+l::
Send ^+{Right}
return

;mark text to the left (with Alt + Shift + J) (default would be Ctrl+Shift+direction)
!+j::
Send ^+{Left}
return

;mark text up
!+i::
Send ^+{up}
return

;mark text down
!+k::
Send ^+{down}
return

;mark text to the end
!+ö::
SendPlay ^+{End}
return

;mark text to home
!+h::
Send ^+{Home}
return

;alternative escape: Alt+N
!n::
Send {Esc}
return



;moving the windows, works nice with PowerToys FancyZones
; -move windows left/right/down/up with win+I,J,K,L
<#j:: SendInput,#{LEFT}
<#l:: SendInput,#{RIGHT}
<#i:: SendInput,#{UP}
<#k:: SendInput,#{DOWN}



;music player shortcuts

;next song: Alt+Ctrl+Right
!^Right:: 
Send {Media_Next}
return

;previous song
!^Left::
Send {Media_Prev}
return

;play/pause
!^Up::
Send {Media_Play_Pause}
return
```
