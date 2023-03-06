**THIS IS THE TXT FILE WHERE I USED TO TRACK MY PROGRESS AND ANYTHING NEW'S LEARNED, BEFORE MARDOWN WAS USED** 
  Project no/name: 
In this project, we'll study:

123. Reset CSS
  - search 'normalize css' -> link css 
124. Setup base CSS
  - using embeded google font 
125. Dựng khung web
  - Naming according to BEM convention
126. Navbar CSS
  - background-img: linear-gradient(<angle>, color 1, color 2)
  - using grid for header 
  - calling variable: color: var(--text-color)
  - making the sideline |
127. Embbed Font Icons
  - embbed font awesome into css, using all.css
128. CSS Icons
  - align and margining ... .FUCKING HARD 
  - fixing 'Ket noi' show effect
129. Header QR code 
  - position absolute : top 100%
  - firstchild, nthchild(<number>)
      <a href="" class="header-nav__qrlink">
          <img src="./assets/img/google_play.png" alt="" class="header-nav_appimg">
      </a>
      <a href="" class="header-nav__qrlink">
          <img src="./assets/img/app_store.png" alt="" class="header-nav_appimg">
      </a>
      -----
      qrlink:firstchild -> google google_play
      qrlink:nthchild(2) _> chplay 
      consider like qrlink class have 2 children of class img
  - on/off for the qrtab
    . fixing gap bridge between the button and qr tab (the tab disappear)
      --> pseudo class
  - QR TAB: set it to appear after 1 sec: 
    . use animation-fill-mode: forwards
    .
130->133. Header notification css
  - user-select: none -> on text -> not allowed user to scan or copy
    .-web-kit-user-select: in case some browser not support the above command
  - animation
    .transform origin
  - CREATE ARROW: using border for nonwidth/height object
    .span{
      border: 20px solid;
      border-color: red transparent transparent transparent;
    }
    -> down red arrow
    . to set from square to triangle -> adjust border width: (ex: 20px 26px)
  - advanced knowledge
      animation: xxx
    . will-change: <animation pro1>, <ani..2>,... 
      -> tell the browser to improve smoothness for animation
    . --webkit-animaion, -moz-animaion,... supporting some browsers
      -> to check: caniuse.com
134-139. Modal for resgiration / signing in
  --Registeration Form 
  - border color: #dbdbdb
  - set outline=none and border corlor for input:focus
  -  css btn classs -> communal class -> base.css
  - communal class 'btn' -> set min-width > width
  - btn-primary -> have to be associated with btn
    -> .btn.btn-primary{}
  - class '.btn.btn-disabled'

  --Signing in Form
  - line-height = 0 -> = minimum height of text

140-145. Header with Search bar 
  - svg img: copy outer html to get svg html -> HTML formatter.com to format the code -> paste
  - use VARIABLES for set height of header, header-nav, header-withsearch
  - box-shadow  
  - History list: 
    . fixing input text does align center -> set height 100%
    . set width = calc(100% - 16px) ~ top
    . css selector: FOCUS for display history search
      + focus go with ~
      + fixing event 'closing history' happens before an a tag is clicked 
  - Cart 
    . line-height=100% -> to remove useless space between

146. Profile Icon
  - icon not align equally -> display flex to parent ul
  
148-161 Product list
  - category
  - filter and paging bar
    . using firstchild/lastchild for border between 2 arrow btns
  - product list 
    . use background-img for item
    . MAKE the '...' at the end of item name (check at class product__name)
      + for suporting browser: 
            overflow: hidden
            height: 2rem; /*Maximum height of name = n*line-height*/
            display: block; /*in case browser does not support webkit*/
            display: -webkit-box;
            -webkit-box-orient: vertical; /*specify which direction the box its text*/
            -webkit-line-clamp: 2; /*allows box to limit its content to a specify number of lines*/
      + for not supporting browser: 
            white-space: nowrap; / overflow:hidden;
            text-overflow: ...
            -> The text-overflow property specifies how overflowed content that is 
            not displayed should be signaled to the user. It can be clipped, display 
            an ellipsis (...), or display a custom string.
    . use "MARGIN-LEFT" : auto to save a div tag at the product__rating 
      (when before i use a parent div to contain -> then justify-content)
      ->> margin-left auto push the el to the right until it hit another el
    . Create the TRIANGLE-EDGE for the favorite label
      + similar to creating the arrow but: 
    . use 'currentcolor' for label
    . Create the DOUBLE TRIANGLE-BOTTOM EDGE for the sales label
      + use border as when create an arrow, but cut the box into half by display none border top
    . Fix UI Bugs 2:
      + cartinfo tab: make a scroll
      + limit name length for cartinfo tab item

162. Pagination UI
  - because it can be reusable in other pages -> css in base.css

164. Footer



RESPONSIVE WEB SHOPEE:
30. Header search box
  - using label - input for enable/disable header search box
31. Products
  - overflow:hidden for wrapper to avoid white space on the left of the site
32. Mobile Categories
  - To make the nav categories able to scroll horizontally
    . max-width: 100% and overflow-x:auto;
  - pseudo class to color category items: nth of type
  - hide scrollbar by: 
    .<class>::-webkit-scrollbar{ display: none}
  - unallow user to select text on mobile: 
    . user-selected: none + -webkit-user-selected: none
  - disable hightlight when tapping btn
    . -webkit-tap-hightlight-color: transparent;
progress: make the section displaying number of items in cart
