---
layout: post
title: My xterm Theme
---

bc.. XTerm*locale: true
XTerm*utf8Title: true
XTerm*fontMenu*fontdefault*Label: Default
XTerm*xftAntialias: true
XTerm*faceName: monaco:antialias=True:pixelsize=14
XTerm*faceNameDoublesize: WenQuanYi Zen Hei Mono:antialias=True:pixelsize=13
XTerm*faceSize: 20
XTerm*faceSize1: 20
XTerm*faceSize2: 20
XTerm*faceSize3: 20
XTerm*faceSize4: 20
XTerm*faceSize5: 20
XTerm*faceSize6: 20
XTerm.cjkWidth: false
XTerm*background: black
XTerm*foreground: gray
XTerm*scrollBar: true
XTerm*rightScrollBar: true
XTerm*jumpScroll: true
XTerm*SaveLines: 30000
*VT100*translations: #override \n\
Shift <KeyPress> Insert:insert-selection(CLIPBOARD, CUT_BUFFER1) \n\
~Shift~Ctrl<Btn2Up>: insert-selection(PRIMARY, CUT_BUFFER0) \n\
~Shift<BtnUp>: select-end(CLIPBOARD, CUT_BUFFER1) \n\
~Shift<BtnUp>: select-end(PRIMARY, CUT_BUFFER0)
