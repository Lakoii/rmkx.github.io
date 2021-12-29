/**
* @name         Duality
* @description  Enjoy Discord with a theme based on elements that "pop out" of the screen.
* @donate       https://bit.ly/3fnzq1Z
* @source       https://github.com/rmkx/rmkx.github.io/blob/main/Duality/src/duality.css
* @author       rmkx
* @invite       HnGWVQbQBv
* @version      1.0.1
*/  

@import url('https://rmkx.github.io/src/settingsIcons.css');
@import url('https://rmkx.github.io/src/customBadges.css');

:root {

    /*Background settings*/

    --app-background: url('https://i.imgur.com/WdSrxA0.jpg'); /*App background*/
    --app--bg-opacity: 0.40; /*App background opacity*/
    --background-image: url('https://images4.alphacoders.com/962/962077.jpg'); /*Main background image*/
    --bg-blur: 0px; /*Main background blur*/
    --bg-opacity: 0; /*Main background opacity*/
    --popout-bg: url('https://i.imgur.com/wQLLZBE.png'); /*Background for popouts*/
    --popout-blur: 0px; /*Popout background blur*/
    --popout-opacity: 0; /*Popout background opacity*/

    /*General Settings*/

    --home-icon-image: url('https://i.imgur.com/eIcueYp.gif'); /*Home icon*/
    --main-dark-color: 21, 21, 21; /*Main dark color of the theme | WARNING: USE RGB VALUES IF YOU CHANGE THE COLOR | Default 21, 21, 21*/
    --scrollbar-dark-color: 6, 6, 6; /*Main dark color of the theme | WARNING: USE RGB VALUES IF YOU CHANGE THE COLOR | Default 21, 21, 21*/
    --window-padding: 50px; /*Change to modify window size | Default 50px*/
    --window-border-radius: 12px; /*Modifies the main window border-radius | Default 12px*/
    --main-radius: 12px; /*Modifies the border-radius of most elements | Default 12px*/
    --settings-width: 60%; /*Width for the settings window | Default 60%*/
    --settings-heigth: 85%; /*Width for the settings window | Default 85%*/
    --embed-border: 0px; /*Makes it so some embeds in chat have their corresponding border | 0px = no borders*/
    --button-radius: 8px; /*Radius for the buttons | Default 8px*/
    --accent-color: 142, 255, 174; /*Main accent | WARNING: USE RGB VALUES IF YOU CHANGE THE COLOR | Default 142, 255, 174*/

    /*Text settings*/
    --server-channel-textc: 198, 198, 198; /*Text color for some elements | WARNING: USE RGB VALUES IF YOU CHANGE THE COLOR | Default 157, 157, 157*/
}

.theme-dark,
.theme-light {
    --text-link: rgb(var(--accent-color));
}

/*Background*/

#app-mount::before { /*Background 1*/
    content: "";
    background: var(--app-background);
    background-position: center;
    background-size: cover;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: -2;
}
#app-mount::after { /*Background 1*/
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(0,0,0, var(--app--bg-opacity));
    z-index: -1;
}
#app-mount .container-2lgZY8::before { /*Background 2*/
    content: "";
    background: var(--background-image);
    background-position: center;
    background-size: cover;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    filter: blur(var(--bg-blur));
    z-index: -2;
}
#app-mount .container-2lgZY8::after { /*Background 2*/
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(0,0,0, var(--bg-opacity));
    z-index: -1;
}
.appMount-3lHmkl,
body,
.app-2rEoOp,
.scroller-1Bvpku,
.wrapper-3NnKdC,
.bg-h5JY_x,
.sidebar-2K8pFh,
.container-3w7J-x,
.chat-3bRxxu,
.members-1998pB,
.members-1998pB .content-3YMskv,
.container-1r6BKw.themed-ANHk51,
.scroller-1JbKMe,
.privateChannels-1nO12o,
.nowPlayingColumn-2sl4cE,
.outer-1AjyKL { /*Transparent panels*/
    background-color: transparent;
}
.container-1D34oG { /*Transparent panels 2*/
    background: transparent!important;
}

/*Scrollbar settings*/

::-webkit-scrollbar-thumb {
    background-color: rgb(var(--scrollbar-dark-color))!important;
    filter: brightness(2%);
    border-radius: var(--main-radius);
}
::-webkit-scrollbar-track {
    background-color: transparent!important;
    border-radius: var(--main-radius);
}

/*Discord main modals*/

.app-2rEoOp { /*Main Discord class*/
    padding: var(--window-padding, 50px);
    z-index: 1;
}
.layers-3iHuyZ { /*Changes borders*/
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569);
    border-radius: var(--window-border-radius, 12px);
}
.backdrop-1wrmKB {
    background: rgba(0, 0, 0, 0.569)!important;
    backdrop-filter: blur(3px);
}

/*Windows bar related*/

.winButton-iRh8-Z { /*Main container*/
    left: calc(-1 * var(--window-padding) - 20px);
    top: calc(var(--window-padding) + 30px);
}
.winButton-iRh8-Z svg { /*Main container icon svg*/
    display: none;
}
.winButton-iRh8-Z::before { /*Main container icons*/
    content: '';
    position: relative;
    left: 0;
    width: 24px;
    height: 24px;
    background: currentColor;
    background-size: contain;
    background-repeat: no-repeat;
    -webkit-mask: url('https://rmkx.github.io/svg/windowsIcons.svg');
    transform: scale(1.3);
    filter: opacity(0.5) brightness(0.65);
    transition: filter 0.25s ease;
}
.winButton-iRh8-Z:hover::before { /*Main container icons hovered*/
    filter: opacity(1);
}
.winButtonClose-1HsbF- { /*Windows close button*/
    color: red;
}
.winButtonClose-1HsbF-:hover { /*Windows close button hovered*/
    background-color: transparent;
    color: red;
}
.winButtonMinMax-PBQ2gm { /*Windows minimaze/maximize buttons*/
    color: rgb(var(--main-dark-color));
}
.winButtonMinMax-PBQ2gm:hover { /*Windows minimaze/maximize buttons hovered*/
    background-color: transparent;
    color: rgb(var(--main-dark-color));
}
.wordmark-2iDDfm { /*Discord Wordmark*/
    color: transparent;
}
.withFrame-haYltI::after { /*Wordmark*/
    content: "DUALITY";
    position: absolute;
    font-size: 1rem;
    color: rgba(var(--server-channel-textc), 0.5)!important;
    left: 0.8%;
    top: 1%;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}

/*Settings Window*/

.layer-3QrUeG.baseLayer-35bLyl { /*Makes it so the background stays/doesn't open a new "window"*/
    opacity: unset!important;
    transform: unset!important;
}
.layer-3QrUeG { /*Settings background*/
    background-color: rgba(0, 0, 0, 0.569);
}
.layers-3iHuyZ > .layer-3QrUeG.stop-animations:first-child > .container-2lgZY8 > .base-3dtUhz > .content-98HsJk,
.layers-3iHuyZ > .layer-3QrUeG.stop-animations:first-child > .container-2lgZY8 > .guilds-1SWlCJ { /*Blurs the background behind the settings window*/
    filter: blur(2px);
    z-index: 0;
}
.standardSidebarView-3F1I7i { /*Modifies the settings window*/
    -webkit-backface-visibility: hidden;
    -webkit-perspective: 1000;
    -webkit-transform: translate3d(0,0,0);
    -webkit-transform: translateZ(0);
    backface-visibility: hidden;
    perspective: 1000;
    transform: translate3d(0,0,0);
    transform: translateZ(0);
    position: absolute;
    top: 50%!important;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
    width: var(--settings-width);
    height: var(--settings-heigth);
    background: transparent;
    border-radius: var(--window-border-radius);
    pointer-events: all;
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569), -3px -6px 10px 10px rgba(0, 0, 0, 0.569);
}
.standardSidebarView-3F1I7i::before { /*Settings window background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--window-border-radius);
    background: var(--popout-bg) center/cover no-repeat;
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.standardSidebarView-3F1I7i::after { /*Settings window background opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--window-border-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.sidebarRegionScroller-3MXcoP,
.contentRegion-3nDuYy,
.contentRegionScroller-26nc1e { /*Subcontainers background*/
    background: transparent;
}
.sidebarRegionScroller-3MXcoP { /*Main window left panel radius*/
    border-top-left-radius: var(--window-border-radius);
    border-bottom-left-radius: var(--window-border-radius);
}
.contentRegion-3nDuYy,
.contentRegionScroller-26nc1e,
.contentTransitionWrap-3hqOEW { /*Main window right panel radius*/
    border-top-right-radius: var(--window-border-radius);
    border-bottom-right-radius: var(--window-border-radius);
}
.closeButton-1tv5uR { /*Close button style*/
    border-color: transparent!important;
}
.closeButton-1tv5uR path { /*Close button style*/
    fill: rgb(var(--server-channel-textc), 0.35)!important;
}
.container-1sFeqf .keybind-KpFkfr { /*ESC text*/
    color: rgb(var(--server-channel-textc), 0.35);
}
.closeButton-1tv5uR svg,
.closeButton-1tv5uR path,
.container-1sFeqf .keybind-KpFkfr { /*Close button/ESC text animation*/
    transition: .25s ease;
}
.closeButton-1tv5uR:hover { /*Close button hover*/
    background-color: transparent!important;
}
.closeButton-1tv5uR:hover svg {
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.closeButton-1tv5uR:hover path { /*Close button hover*/
    fill: rgb(var(--server-channel-textc), 1)!important;
}
.closeButton-1tv5uR:hover+.keybind-KpFkfr { /*Close button hover*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
    color: rgb(var(--server-channel-textc), 1)!important;
}
.closeButton-1tv5uR::before { /*Close button left backdrop*/
    content: '';
    position: fixed;
    top: calc(0% - calc(100% - var(--settings-heigth)));
    left: -40%;
    width: calc(100% - var(--settings-width));
    height: 2000px;
    cursor: pointer;
    pointer-events: inherit;
    transition: 0.25s ease-in;
}
.closeButton-1tv5uR::after { /*Close button right backdrop*/
    content: '';
    position: fixed;
    top: calc(0% - calc(100% - var(--settings-heigth)));
    left: 100%;
    width: calc(100% - var(--settings-width));
    height: 2000px;
    cursor: pointer;
    pointer-events: inherit;
    transition: 0.25s ease-in;
}
.closeButton-1tv5uR:active { /*Makes the window dissapear*/
    transform: none;
}
.background-1QDuV2,
.fieldList-21DyL8 { /*Account details main panels*/
    background: transparent;
}
.divider-3573oO { /*Settings category divider*/
    height: unset;
    border-top: unset;
}
.container-3auIfb { /*Checked buttons*/
    border-radius: var(--general-radius);
}
.container-3auIfb[style*="background-color: hsl(218, calc(var(--saturation-factor, 1) * 4.6%), 46.9%);"] { /*Unchecked buttons*/
    border-radius: var(--button-radius);
    background-color: transparent!important;
}
.container-3auIfb[style*="background-color: hsl(218, calc(var(--saturation-factor, 1) * 4.6%), 46.9%);"]::before { /*Unchecked buttons background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    border-radius: var(--button-radius);
    background-color: rgb(var(--main-dark-color))!important;
    filter: brightness(20%);
}
.container-3auIfb[style*="background-color: hsl(139, calc(var(--saturation-factor, 1) * 47.3%), 43.9%);"] { /*Checked buttons color*/
    border-radius: var(--button-radius);
    background-color: transparent!important;
}
.container-3auIfb[style*="background-color: hsl(139, calc(var(--saturation-factor, 1) * 47.3%), 43.9%);"]::before { /*Checked buttons background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    border-radius: var(--button-radius);
    background-color: rgb(var(--accent-color))!important;
    filter: brightness(0.35);
}
.container-3auIfb[style*="background-color: hsl(139, calc(var(--saturation-factor, 1) * 47.3%), 43.9%);"] svg svg path,
.container-3auIfb[style*="background-color: hsl(218, calc(var(--saturation-factor, 1) * 4.6%), 46.9%);"] svg svg path { /*Checkmark svg*/
    display: none;
}
.cardPrimary-1Hv-to { /*Card in bottom settings*/
    border: none;
    background-color: transparent;
}
.side-8zPYf6 .separator-gCa7yv { /*Settings category divider*/
    height: 0px;
}
.hero-EvfTTA { /*Discord nitro banner*/
    background-image: url('');
    height: 250px;
}
.marketingRefreshSectionTier1-dRwS-6 { /*Discord nitro classic panel*/
    border-top: none;
    margin-top: unset;
}
.marketingRefreshSectionTier1-dRwS-6 .buttons-2-EdE8 { /*Discord nitro classic panel buttons*/
    transform: translateX(-5.5%);
}
.feature-2w65J5,
.cardWrapper-2Min21 { /*Nitro cards/Server boosts*/
    border: 1px solid rgb(var(--server-channel-textc));
    border-radius: 8px;
    background: transparent!important;
    transition: filter 0.25s ease;
}
.feature-2w65J5:hover,
.cardWrapper-2Min21:hover { /*Nitro cards/Server boosts hovered*/
    background: transparent!important;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.card-3AyPWq:hover { /*Server boosts hovered*/
    background-color: transparent;
}
.wrapper-3nSjSv,
.upsellContainer-3UlEOE { /*Nitro deals background*/
    background: transparent;
}
.tier-1EY-yj { /*Nitro tier*/
    border: 1px solid rgb(var(--server-channel-textc));
    border-radius: 8px;
    background: transparent!important;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.codeRedemptionRedirect-1wVR4b { /*Billind code panel*/
    background-color: transparent!important;
    border: none!important;
}
.side-8zPYf6 .item-PXvHYJ:not(.selected-3s45Ha):not([aria-controls="Discord Nitro-tab"]):not([aria-controls="GUILD_PREMIUM-tab"]) { /*Settings category*/
    color: rgb(var(--server-channel-textc));
    filter: opacity(0.35);
    transition: filter 0.25s ease;
}
.side-8zPYf6 .item-PXvHYJ:not(.selected-3s45Ha):not([aria-controls="Discord Nitro-tab"]):not([aria-controls="GUILD_PREMIUM-tab"]):hover { /*Settings category hovered*/
    color: rgb(var(--server-channel-textc));
    background-color: transparent!important;
    filter: opacity(0.65) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.side-8zPYf6 .themed-OHr7kt.selected-3s45Ha.item-PXvHYJ { /*Settings category selected*/
    color: rgb(var(--server-channel-textc));
    background-color: transparent;
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.side-8zPYf6 .themed-OHr7kt.selected-3s45Ha.item-PXvHYJ:hover { /*Settings category selected*/
    color: rgb(var(--server-channel-textc));
    background-color: transparent;
}
.side-8zPYf6 .item-PXvHYJ[aria-controls="Discord Nitro-tab"]:not([aria-selected="true"]),
.side-8zPYf6 .item-PXvHYJ[aria-controls="GUILD_PREMIUM-tab"]:not([aria-selected="true"]) { /*Discord category main container*/
    color: rgb(var(--server-channel-textc))!important;
    filter: opacity(0.35);
    transition: filter 0.25s ease;
}
.side-8zPYf6 .item-PXvHYJ[aria-controls="Discord Nitro-tab"]:not([aria-selected="true"]):hover,
.side-8zPYf6 .item-PXvHYJ[aria-controls="GUILD_PREMIUM-tab"]:not([aria-selected="true"]):hover { /*Discord category main container hovered*/
    color: rgb(var(--server-channel-textc))!important;
    background-color: transparent!important;
    filter: opacity(0.65) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.side-8zPYf6 .item-PXvHYJ[aria-controls="Discord Nitro-tab"][aria-selected="true"],
.side-8zPYf6 .item-PXvHYJ[aria-controls="GUILD_PREMIUM-tab"][aria-selected="true"] { /*Discord category selected*/
    color: rgb(var(--server-channel-textc))!important;
    background-color: transparent!important;
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.contentColumnDefault-1VQkGM .defaultColor-1_ajX0, /*Category section title*/
.contentColumnDefault-1VQkGM .h5-18_1nd { /*Category section subtitle*/ 
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.contentColumnDefault-1VQkGM .h5-18_1nd { /*Category section subtitle*/
    font-size: 0.8rem;
}
.contentColumnDefault-1VQkGM .children-rWhLdy .fieldTitle-3h2iLW { /*User info sections*/
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
    margin-bottom: 8px;
}
.contentColumnDefault-1VQkGM .children-rWhLdy .fieldSpacer-wgewFh { /*User info separation*/
    margin-top: 12px;
}
.cardPrimaryOutline-29Ujqw { /*Authorized app*/
    border: 1px solid;
    color: rgb(var(--server-channel-textc));
    border-color: rgba(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.cardPrimaryOutline-29Ujqw .h5-18_1nd { /*Authorized app subtitle*/
    filter: none;
}
.cardPrimaryOutline-29Ujqw:hover { /*Authorized app hovered*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
    border-color: rgba(var(--server-channel-textc), 1);
}
.accountList-33MS45 { /*Connect account list*/
    background-color: transparent;
}
.connectedAccounts-2-XP1G .accountBtn-2Nozo3 .accountBtnInner-sj5jLs { /*Conneted accounts list icons*/
    background-color: transparent;
    transition: filter 0.25s ease;
}
.connectedAccounts-2-XP1G .accountBtn-2Nozo3 .accountBtnInner-sj5jLs:hover { /*Conneted accounts list icons*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.connection-1fbD7X,
.connectionHeader-2MDqhu,
.integration-3kMeY4 { /*Discord connected account*/
    background-color: transparent;
}
.connection-1fbD7X { /*Discord connected account main panel*/
    border: 1px solid;
    color: rgb(var(--server-channel-textc));
    border-color: rgba(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.connection-1fbD7X:hover { /*Discord connected account main panel*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
    border-color: rgba(var(--server-channel-textc), 1);
}
.radioBar-bMNUI- { /*Privacy and safety DM border*/
    border-color: transparent!important;
}
.item-26Dhrx,
.item-26Dhrx[aria-checked=true] { /*Privacy and safety DM settings*/
    background-color: transparent;
    border-radius: var(--main-radius);
}
.item-26Dhrx:hover:not([aria-checked=true]) { /*Privacy and safety DM settings hovered*/
    background-color: transparent;
}
@keyframes selectedCircle {
    0% {
        color: transparent;
    }
    100% {
        color: rgb(var(--main-accent));
    }
}
.radioIconForeground-XwlXQN { /*Selected item radio group*/
    animation: selectedCircle 0.25s ease;
    animation-fill-mode: forwards;
}
.item-26Dhrx .info-3LOr12,
.item-26Dhrx svg { /*Radio group text*/
    filter: opacity(0.35);
    color: rgb(var(--server-channel-textc));
    transition: filter 0.25s ease;
}
.item-26Dhrx:hover:not([aria-checked=true]) .info-3LOr12, 
.item-26Dhrx:hover:not([aria-checked=true]) svg { /*Radio group hovered*/
    filter: opacity(0.65) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.item-26Dhrx[aria-checked=true] .info-3LOr12,
.item-26Dhrx[aria-checked=true] svg { /*Radio group checked text*/
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.children-rWhLdy div[aria-labelledby] .item-26Dhrx::before { /*Privacy option animation*/
    transition: filter 0.25s ease;
}
.children-rWhLdy div[aria-labelledby] .item-26Dhrx:first-child::before { /*First privacy option*/
    content: '';
    position: absolute;
    top: 10.3%;
    left: 11%;
    height: 1px;
    width: 80%;
    border-bottom: 1px solid rgb(67, 181, 129);
    filter: opacity(0.35);
}
.children-rWhLdy div[aria-labelledby] .item-26Dhrx:nth-child(2)::before { /*Second privacy option*/
    content: '';
    position: absolute;
    top: 13.8%;
    left: 11%;
    height: 1px;
    width: 80%;
    border-bottom: 1px solid rgb(250, 166, 26);
    filter: opacity(0.35);
}
.children-rWhLdy div[aria-labelledby] .item-26Dhrx:last-child::before { /*Last privacy option*/
    content: '';
    position: absolute;
    top: 17.3%;
    left: 11%;
    height: 1px;
    width: 80%;
    border-bottom: 1px solid rgb(240, 71, 71);
    filter: opacity(0.35);
}
.children-rWhLdy div[aria-labelledby] .item-26Dhrx:first-child:hover:not([aria-checked=true])::before,
.children-rWhLdy div[aria-labelledby] .item-26Dhrx:nth-child(2):hover:not([aria-checked=true])::before,
.children-rWhLdy div[aria-labelledby] .item-26Dhrx:last-child:hover:not([aria-checked=true])::before { /*Hovered privacy options*/
    filter: opacity(0.65) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.children-rWhLdy div[aria-labelledby] .item-26Dhrx[aria-checked=true]::before { /*Selected privacy option*/
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.warning-3C2pOH { /*Warning message*/
    border-radius: var(--button-radius);
    background: transparent;
    color: var(--info-warning-foreground);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.row-2okwlC { /*Divider between keybinds*/
    box-shadow: none!important;
}
.card-FDVird:before { /*Keybind card*/
    background-color: transparent!important;
    border-color: transparent!important;
}
.container-CpszHS { /*Keybind recording container*/
    background-color: transparent;
    border-radius: var(--button-radius);
    border-color: rgba(var(--server-channel-textc), .35)!important;
    transition: 0.25s ease;
}
.container-CpszHS:hover { /*Keybind recording container*/
    background-color: transparent;
    border-radius: var(--button-radius);
    border-color: rgba(var(--server-channel-textc), 1)!important;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.keybindShortcut-1BD6Z1 span { /*Keybind Shortcut button*/
    background-color: transparent!important;
    border-radius: var(--button-radius);
    border-color: rgb(var(--server-channel-textc))!important;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
    padding-top: 4px;
    box-shadow: unset!important;
    color: rgb(var(--server-channel-textc))!important;
}
.barFill-23-gu- { /*Filled bar color*/
    background: rgba(var(--accent-color), 0.85);
}
.bar-2Qqk5Z {  /*Filled bar background color*/
    background: rgba(var(--scrollbar-dark-color), .5)!important;
}
.defaultValue-3gC7yw .markValue-2DwdXI { /*Defalt text scale color*/
    color: rgba(var(--accent-color), 0.55);
}
.userSettingsVoice-iwdUCU .media-engine-video { /*Camera preview main modal*/
    background-color: transparent;
}
.userSettingsVoice-iwdUCU .previewOverlay-2O7_KC { /*Camera preview window*/
    background-color: transparent!important;
    border-color: transparent!important;
}
.notches-1sAcEM { /*Test voice bar notches*/
    background-image: url()!important;
}
.progress-1IcQ3A { /*Test voice bar progress background*/
    background-color: rgb(var(--scrollbar-dark-color))!important;
}
.container-3PXSwK { /*Test voice bar progress color*/
    background: linear-gradient(to right, rgba(var(--accent-color), 0.25), rgba(var(--accent-color), 1))!important;
}
.inputSensitivityToggle-2LKb8o .bar-2Qqk5Z { /*Voice sensitivity bar*/
    background: rgba(var(--scrollbar-dark-color), 0.45)!important;
}
.inputSensitivityToggle-2LKb8o .barFill-23-gu- { /*Voice sensitivity bar 2*/
    background: rgba(var(--accent-color), 0.85)!important;
}
.notDetected-33MY4s { /*No game detected panel*/
    background-color: transparent!important;
}
.game-1ipmAa { /*Added games*/
    margin-bottom: 3%;
    box-shadow: unset!important;
    transition: filter 0.25s ease;
}
.game-1ipmAa:hover { /*Added games*/
    margin-bottom: 3%;
    box-shadow: unset!important;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.overlayToggleIconOn-3UNmty .fill-1ugeBG { /*Overlay Icon ON*/
    fill: rgba(var(--accent-color), 0.85)!important;
    transition: 0.25s ease;
}
.overlayToggleIcon-2liB3r:hover .overlayToggleIconOn-3UNmty { /*Overlay Icon ON hover*/
    filter: brightness(0.4);
    transition: 0.25s ease;
}
.overlayToggleIcon-2liB3r:hover .overlayToggleIconOn-3UNmty .fill-1ugeBG path{ /*Overlay Icon ON hover 2*/
    fill: #f04747!important;
    transition: 0.25s ease;
}
.overlayToggleIcon-2liB3r:hover .overlayToggleIconOn-3UNmty path {/*Overlay Icon ON hover 3*/
    fill: #f04747!important;
    d: path("M 8.67872 19 H 11 V 21 H 7 V 23 H 17 V 21 H 13 V 19 H 20 C 21.103 19 22 18.104 22 17 V 6 C 22 5.89841 21.9924 5.79857 21.9777 5.70101 L 20 7.67872 V 15 H 12.6787 L 8.67872 19 Z M 13.1496 6 H 4 V 15 H 4.14961 L 2.00515 17.1445 C 2.00174 17.0967 2 17.0486 2 17 V 6 C 2 4.897 2.897 4 4 4 H 15.1496 L 13.1496 6 Z");
    transition: 0.25s ease;
}
.overlayToggleIconOff-1kT42w .fill-1ugeBG,
.overlayToggleIconOff-1kT42w rect { /*Overlay Icon OFF*/
    transition: 0.25s ease;
}
.overlayToggleIcon-2liB3r:hover .overlayToggleIconOff-1kT42w .fill-1ugeBG { /*Overlay Icon OFF hover*/
    fill: rgba(var(--accent-color), 0.4)!important;
    transition: 0.25s ease;
}
.overlayToggleIcon-2liB3r:hover .overlayToggleIconOff-1kT42w path {
    d: path("M 4 2.5 C 2.897 2.5 2 3.397 2 4.5 V 15.5 C 2 16.604 2.897 17.5 4 17.5 H 11 V 19.5 H 7 V 21.5 H 17 V 19.5 H 13 V 17.5 H 20 C 21.103 17.5 22 16.604 22 15.5 V 4.5 C 22 3.397 21.103 2.5 20 2.5 H 4 Z M 20 4.5 V 13.5 H 4 V 4.5 H 20 Z");
    transition: 0.25s ease;
}
.overlayToggleIcon-2liB3r:hover .overlayToggleIconOff-1kT42w rect {
    display: none;
    transition: 0.25s ease;
}
.game-1ipmAa .removeGame-2JFGPn { /*Remove game button*/
    background-color: transparent;
    box-shadow: unset;
    filter: brightness(0.55);
    transition: 0.25s ease;
}
.game-1ipmAa .removeGame-2JFGPn:hover { /*Remove game button hover*/
    background-color: transparent;
    box-shadow: unset;
    filter: brightness(1);
    transition: 0.25s ease;
}
.wrapper-3jrx9n { /*Overlay position*/
    border-radius: 8px;
    border-color: rgba(var(--server-channel-textc), .35);
    transition: .25s ease;
}
.wrapper-3jrx9n:hover { /*Overlay position*/
    border-color: rgba(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.option-n0icdO { /*Overlay position options*/
    border-radius: 5px;
    background-color: rgba(var(--main-dark-color), .5);
    transition: background-color 0.25s ease;
}
.option-n0icdO:hover { /*Overlay position option hovered*/
    background-color: rgba(var(--accent-color), .35);
    transition: background-color 0.25s ease;
}
.selected-mKYnfr.option-n0icdO { /*Selected overlay position*/
    background-color: rgba(var(--accent-color), .65);
    border-color: rgba(var(--accent-color), .65);
    transition: 0.25s ease;
}
.disabledIcon-9QatvX { /*Disabled overlay option*/
    transition: 0.25s ease;
}
.root-1gCeng { /*Changelog modal*/
    background: transparent;
    border-radius: var(--main-radius);
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569)!important;
}
.root-1gCeng::before { /*Changelog modal background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background: var(--popout-bg) center/cover no-repeat;
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.root-1gCeng::after { /*Changelog modal opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.footer-2gL1pp { /*Changelog modal footer*/
    box-shadow: unset!important;
    background-color: transparent!important;
    border-radius: var(--general-radius);
}
.featureBorder-7j4v58 { /*Hypesquad divider*/
    border: none;
}
.previewMessage-1ZN7YG,
.preview-2nSL_2 { /*Previews*/
    background-color: transparent;
}
.accountProfileCard-1XCH88,
.profileBannerPreview-3_l0Wd { /*User card info*/
    background-color: transparent;
}
.avatarUploaderInner-Oiob_P,
.avatar-1uQSZT { /*New avatar uploader*/
    border: none;
    background-color: transparent;
}

/*BD settings*/

.bd-switch-body { /*BD checkbox default/unchecked*/
    border-radius: var(--button-radius);
    --switch-color: transparent;
}
.bd-switch-body::before { /*BD checkbox default/unchecked background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--button-radius);
    background-color: rgb(var(--main-dark-color));
    filter: brightness(0.2);
}
.bd-switch input:checked+.bd-switch-body { /*BD checked checkbox*/
    border-radius: var(--button-radius);
    --switch-color: transparent;
}
.bd-switch input:checked+.bd-switch-body::before { /*BD checked checkbox background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--button-radius);
    background-color: rgb(var(--accent-color));
    filter: brightness(0.35);
}
.bd-setting-divider { /*BD settings divider*/
    border-color: transparent;
}
.bd-settings-group.collapsible .bd-settings-title::before,
.bd-settings-group.collapsible .bd-settings-title::after { /*Line after settings section title expanded*/
    background-color: rgb(var(--accent-color));
    filter: brightness(.85);
    transition: 0.25s ease-in;
}
.bd-settings-group.collapsed .bd-settings-title::before,
.bd-settings-group.collapsed .bd-settings-title::after { /*Line after settings section title collapsed*/
    background-color: rgb(var(--accent-color));
    filter: brightness(0.35);
    transition: 0.25s ease;
}
.bd-button { /*BD blue buttons*/
    border-radius: var(--button-radius);
    border: 1px solid;
    color: rgba(var(--server-channel-textc), .65);
    background-color: transparent;
    transition: 0.25s ease;
}
.bd-button:hover { /*BD blue buttons hovered*/
    background-color: transparent;
    color: rgba(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.bd-addon-views .bd-view-button svg { /*View style buttons*/
    fill: rgb(var(--server-channel-textc))!important;
    filter: opacity(0.35);
    transition: .25s ease;
}
.bd-addon-views .bd-view-button.selected svg { /*View style selected button*/
    filter: opacity(1);
}
.bd-addon-views .bd-view-button.selected { /*BD button selected view*/
    border-radius: var(--button-radius);
    color: rgba(var(--server-channel-textc), 1);
    background-color: transparent;
    transition: 0.25s ease;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.bd-view-button { /*BD view button*/
    color: rgba(var(--server-channel-textc), .35);
    transition: 0.25s ease;
}
.bd-view-button:hover { /*BD view button hovered*/
    background-color: transparent!important;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
    color: rgba(var(--server-channel-textc), .85);
    transition: 0.25s ease;
}
.bd-view-button:hover:not(.selected) svg { /*BD view button hovered svg*/
    filter: opacity(0.85)!important;
}
.bd-search-wrapper { /*BD searchbar*/
    border: 1px solid rgba(var(--server-channel-textc), .35);
    border-radius: var(--button-radius);
    background-color: transparent;
    transition: border-color 0.25s ease;
}
.bd-search-wrapper:hover { /*BD searchbar hovered*/
    border-color: rgba(var(--server-channel-textc), .65);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
    transition: 0.25s ease;
}
.bd-search-wrapper:focus-within { /*BD searchbar focused*/
    border-color: rgba(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.bd-addon-list .bd-addon-card { /*BD addon container*/
    border: 1px solid rgba(var(--server-channel-textc), 0.35);
    border-radius: var(--button-radius);
    background-color: rgba(var(--main-dark-color), .25);
    transition: 0.25s ease;
}
.bd-addon-list .bd-addon-card:hover {
    background-color: transparent;
    border-color: rgba(var(--server-channel-textc), 1);
    background-color: rgba(var(--main-dark-color), .25);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.bd-addon-list .bd-addon-header { /*BD addon container header*/
    background-color: transparent;
}
.bd-changelog-modal code.inline { /*Inline code*/
    background: rgba(0,0,0,0.35);
}
.bd-controls>.bd-addon-button:first-of-type { /*Theme buttons*/
    border-radius: var(--button-radius) 0 0 var(--button-radius);
}
.bd-controls>.bd-addon-button:last-of-type {
    border-radius: 0 var(--button-radius) var(--button-radius) 0;
    background-color: transparent;
}

/*Dropboxes*/

.css-gvi9bl-control,
.css-1kj8ui-container,
.bd-select { /*Main input device dropbox*/
    background-color: transparent;
    border-radius: var(--button-radius);
    border-color: rgba(var(--server-channel-textc), .35);
    transition: 0.25s ease;
    z-index: 3;
}
.css-17e1tep-control,
.css-17e1tep-control:focus,
.css-17e1tep-control:active { /*Focused main input device dropbox*/
    border-radius: var(--button-radius);
    background-color: transparent;
    border-color: rgba(var(--server-channel-textc), 1)!important;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
    transition: 0.25s ease;
}
.css-gvi9bl-control:hover,
.bd-select:hover { /*Main input device dropbox hovered*/
    background-color: rgba(0, 0, 0, 0.35);
    border-color: rgba(var(--server-channel-textc), 0.5);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0));
    transition: 0.25s ease;
}
.css-6fzn47-control:hover,
.css-6fzn47-control,
.bd-select.menu-open { /*Main input device dropbox selected/focused*/
    border-radius: var(--button-radius) var(--button-radius) 0px 0px;
    border-bottom-color: transparent!important;
    background-color: rgba(0, 0, 0, 0.35);
    backdrop-filter: blur(3px);
    border-color: rgba(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
    transition: 0.25s ease;
}
.css-1ba14n5-option,
.bd-select .bd-select-option.selected { /*Dropdown menu selected option*/
    background-color: transparent;
    color: rgb(var(--accent-color))!important;
}

@keyframes dropDownAnimation {
    0% {
        transform: scaleY(0);
    }
    100% {
        transform: scaleY(1);
    }
}
.css-3vaxre-menu,
.bd-select .bd-select-options { /*Dropdown menu open*/
    border-radius: 0px 0px var(--button-radius) var(--button-radius);
    background-color: rgba(0, 0, 0, 0.35);
    border-color: rgba(var(--server-channel-textc), 1);
    border-top-color: transparent!important;
    animation: dropDownAnimation 0.2s ease-in;
    transform-origin: top;
    backdrop-filter: blur(3px);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
    transition: 0.25s ease;
}
.css-rzbxvl-option,
.bd-select .bd-select-option:hover { /*Hovered main input option*/
    background-color: transparent;
    color: rgba(var(--accent-color), 0.55);
    transition: 0.25s ease;
}
.css-17mfgdg-container .css-118dehu-control { /*Not selectable*/
    background-color: transparent;
    border-radius: var(--button-radius);
    border-color: rgba(var(--server-channel-textc), .15);
    transition: 0.25s ease;
}

/*Blur Username, E-mail and phone in settings*/

.field-1HUseB+.field-1HUseB .colorHeaderPrimary-26Jzh-.size16-1P40sf { /*Blurs e-mail and phone number*/
    filter: blur(8px);
    transition: 0.2s ease;
}
.field-1HUseB+.field-1HUseB .colorHeaderPrimary-26Jzh-.size16-1P40sf:hover { /*Unblurs e-mail and phone number*/
    filter: blur(0px) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.usernameInnerRow-ZlFnET { /*Blurs username*/
    filter: blur(8px);
    transition: 0.2s ease;
}
.usernameInnerRow-ZlFnET:hover { /*Unblurs username*/
    filter: blur(0px) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}

/*Right click menu*/

.menu-3sdvDG { /*Main modal*/
    border-radius: var(--main-radius);
    background-color: transparent;
    background: transparent;
    box-shadow: -3px -6px 10px 4px black;
    animation: menuShow 0.25s ease;
    transform-origin: top;
}
.menu-3sdvDG::before { /*Main modal background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background: var(--popout-bg) center/cover no-repeat;
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.menu-3sdvDG::after { /*Main modal opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.menu-3sdvDG .colorDefault-2K3EoJ,
.menu-3sdvDG .colorDefault-2K3EoJ .label-22pbtT .subtext-13Lvrj { /*Right click menu category*/
    border-color: transparent;
    color: rgba(var(--server-channel-textc), 0.2);
}
.menu-3sdvDG .colorDefault-2K3EoJ .label-22pbtT,
.menu-3sdvDG .colorDefault-2K3EoJ .label-22pbtT .subtext-13Lvrj { /*Menu category base settings*/
    transition: 0.25s ease;
}
.menu-3sdvDG  .colorDefault-2K3EoJ.focused-3afm-j { /*Right click menu category hovered*/
    background-color: transparent;
    color: rgba(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.menu-3sdvDG .colorDefault-2K3EoJ.focused-3afm-j .label-22pbtT .subtext-13Lvrj { /*Menu category subtext hovered*/
    color: rgba(var(--server-channel-textc), 1);
}
.button-F9qN4n { /*Add reaction*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.separator-2I32lJ { /*Server menu*/
    border-bottom: none;
}
.menu-3sdvDG .colorDefault-2K3EoJ.focused-3afm-j .icon-LYJorE { /*Server menu icons*/
    transition: 0.25s ease;
}
.button-F9qN4n:hover,
.keyboard-mode .button-F9qN4n.focused-3ZzkKr { /*Reactions hovered*/
    background-color: transparent;
}

/*Chat settings*/

.form-2fGMdU:before,
.children-19S4PO:after { /*Random pseudoelements*/
    display: none!important;
}
.content-yTz4x3:before { /*Channel description underline*/
    box-shadow: unset;
}
.chat-3bRxxu .toolbar-1t6TWx { /*Inbox, help, etc container*/
    position: absolute;
    right: 7.5%;
    transform: translateX(-7.5%);
}
.toolbar-1t6TWx .clickable-3rdHwn .icon-22AiRD,
.toolbar-1t6TWx .clickable-3rdHwn[aria-checked='false'] .icon-22AiRD { /*Inbox, help, etc icons*/
    color: rgba(255, 255, 255, 0.5);
    transition: 0.35s ease;
}
.toolbar-1t6TWx .clickable-3rdHwn[aria-checked='true'] .icon-22AiRD { /*Inbox, help, etc icons*/
    color: rgba(255, 255, 255, 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.toolbar-1t6TWx .clickable-3rdHwn:not([aria-checked='true']) .icon-22AiRD:hover { /*Inbox, help, etc icons hovered*/
    color: rgba(255, 255, 255, 1);
    filter: drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.toolbar-1t6TWx .clickable-3rdHwn.selected-1GqIat .icon-22AiRD { /*Inbox, help, etc icons selected*/
    color: rgba(255, 255, 255, 1)!important;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0))!important; 
}
.chat-3bRxxu .topic-TCb_qw { /*Channel description*/
    max-width: 55%;
}
.wrapper-3vR61M,
.wrapper-1F5TKx { /*Chat loading messages*/
    background:transparent
}
.scrollerSpacer-avRLaA { /*Space between last message and chat box*/
    height: 10px;
}
.content-1o0f9g { /*Day message*/
    background: transparent;
    border-radius: 3px;
}
.wrapper-2aW0bm,
.full-motion .wrapper-2aW0bm:hover  { /*Reply to/More options main container*/
    background-color: transparent;
    box-shadow: none;
}
.wrapper-2aW0bm .button-1ZiXG9 { /*Reply to/More options buttons*/
    color: rgb(var(--server-channel-textc));
    transition: filter 0.25s ease;
}
.wrapper-2aW0bm .button-1ZiXG9:hover { /*Reply to/More options buttons*/
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-2px 0px 1px rgb(0, 0, 0));
    background-color: transparent;
}
.markup-2BOw-j pre { /*code modal*/
    margin-bottom: 6px;
}
.markup-2BOw-j code { /*code modal*/
    border-radius: var(--main-radius);
    border: none;
    background: rgba(0,0,0,0.35);
}
.hljs-comment { /*Code comment*/
    color: green;
}
.cozy-3raOZG.wrapper-2a6GCs .markup-2BOw-j { /*Chat code modal*/
    padding-bottom: 3px;
}
.embedFull-2tM8-- { /*Chat embed*/
    border-left: var(--embed-border) solid;
    background: rgba(0,0,0,0.35);
    border-radius: var(--main-radius);
}
.wrapper-35wsBm, /*Discord server link*/
.wrapper-2TxpI8 { /*Video embed*/
    background: rgba(0,0,0,0.35)!important;
    border-radius: var(--main-radius)!important;
}
.tileHorizontal-3eee4N { /*Nitro gift embed*/
    background-color: rgba(0,0,0,0.35)!important;
    box-shadow: unset!important;
    border-radius: var(--main-radius);
}
.invalidPoopHorizontal-3Dfy7T { /*Nitro gift embed 2*/
    background-color: transparent!important;
}
.attachment-33OFj0 { /*Attached file*/
    border-color: transparent;
    background-color: rgba(0,0,0,0.35);
    border-radius: var(--main-radius);
}
.wrapperAudio-1jDe0Q { /*Attached audio*/
    border-color: transparent!important;
    background-color: rgba(0,0,0,0.35)!important;
    border-radius: var(--main-radius)!important;
}
.message-2qRu38 { /*Deleting file*/
    background-color: transparent!important;
}
.role-1P70N6,
.role-1P70N6:hover { /*Allowed roles in channel*/
    background-color: transparent;
    transition: filter 0.25s ease;
}
.role-1P70N6:hover { /*Hovered allowed role in channel*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0)); 
}
.operations-36ENbA > a { /*Cancel/save buttons when editing*/
    color: rgba(var(--accent-color), 0.75);
}
.modalTextContainer-ITvzbi { /*Expanded text file*/
    background-color: transparent;
    border-color: transparent;
}
.resultsBlocked-3a77lQ { /*Blocked users results*/
    background-color: transparent;
    border-color: transparent;
}
.invite-18yqGF { /*Spotify invite panel*/
    border-color: transparent!important;
    background-color: transparent!important;
}
.container-1ov-mD > iframe[class="embedSpotify-tvxDCr embedWrapper-lXpS3L"] { /*Spotify embed border*/
    border-radius: 8px!important;
}
.container-1pMiXm { /*File attached main container*/
    border-radius: var(--main-radius);
    background: rgba(0,0,0,0.35);
}
.container-1pMiXm .hljs { /*File attached code preview*/
    box-shadow: none;
}
.container-1pMiXm .textContainer-C0szpm,
.container-1pMiXm .footer-2yA7Ep { /*File attached subcontainers*/
    border: none;
    background-color: transparent;
}
.modalRoot-2o6FJT { /*Expanded file preview main modal*/
    background: transparent;
    background-size: cover;
    border-radius: var(--main-radius);
    top: 50%;
    transform: translateY(-50%)!important;
    height: 90%;
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569)!important;
}
.modalRoot-2o6FJT::before { /*Expanded file preview main modal background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background: var(--popout-bg) center/cover no-repeat;
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.modalRoot-2o6FJT::after { /*Expanded file preview main modal opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.modalContent-3XArPg { /*Expanded file modal*/
    border-radius: var(--main-radius);
}
.modalTextContainer-ITvzbi,
.footer-2yA7Ep { /*File preview main containers*/
    background-color: transparent;
    border: none;
}
.modalTextContainer-ITvzbi {
    overflow-x: auto!important;
    height: 100%;
}
.modalTextContainer-ITvzbi::-webkit-scrollbar-thumb,
.scrollbarGhostHairline-1mSOM1::-webkit-scrollbar-thumb { /*File preview scrollbar*/
    background-color: rgb(var(--server-channel-textc))!important;
}
.card-3RzMcx,
.card-3RzMcx:hover { /*First server steps cards*/
    background-color: transparent;
}
.cozy-3raOZG.wrapper-2a6GCs { /*Chat message settings*/
    transition: filter 0.25s ease;
}
.cozy-3raOZG.wrapper-2a6GCs:hover { /*Chat message hovered settings*/
    background-color: rgb(0, 0, 0, 0.05)!important;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.emptyChannelIcon-cc932w { /*Channel icon in chat*/
    background-color: transparent;
}
.wrapper-3WhCwL { /*Channel linked in chat*/
    color: rgb(var(--accent-color))!important;
    background-color: transparent!important;
}
.group-spacing-16 .divider-3_HH5L .content-1o0f9g {
    color: rgb(var(--server-channel-textc));
    font-size: 0.85rem;
}
.group-spacing-16 .divider-3_HH5L.isUnread-3Ef-o9 { /*Unread new message border*/
    border: 1px solid rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.group-spacing-16 .divider-3_HH5L.isUnread-3Ef-o9:not(.hasContent-1_DUdQ) { /*Unread new message margin*/
    margin: 8px 0 8px 0;
}
.group-spacing-16 .divider-3_HH5L.isUnread-3Ef-o9 .unreadPill-2HyYtt { /*Unread new message tag*/
    background-color: rgb(var(--server-channel-textc));
    overflow: visible!important;
    color: black;
    right: -0.1%;
}
.group-spacing-16 .divider-3_HH5L .unreadPillCapStroke-7rkHbg { /*New message tag*/
    fill: rgb(var(--server-channel-textc));
    color: rgb(var(--server-channel-textc));
}
.group-spacing-16 .divider-3_HH5L.hasContent-1_DUdQ:not(.isUnread-3Ef-o9) { /*New day text*/
    border-color: transparent;
}
.group-spacing-16 .divider-3_HH5L.hasContent-1_DUdQ:not(.isUnread-3Ef-o9) .content-1o0f9g {
    transform: translateY(-3px);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}   
.group-spacing-16 .divider-3_HH5L.hasContent-1_DUdQ:not(.isUnread-3Ef-o9) .content-1o0f9g::before { /*New day text underline*/
    content: '';
    position: absolute;
    left: 50%;
    bottom: -3px;
    transform: translateX(-50%);
    width: 125%;
    height: 2px;
    background: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.group-spacing-16 .divider-3_HH5L.hasContent-1_DUdQ.isUnread-3Ef-o9 { /*Unread new message on new day*/
    top: 5px;
}
.group-spacing-16 .divider-3_HH5L.hasContent-1_DUdQ.isUnread-3Ef-o9 .content-1o0f9g { /*Unread new message on new day text*/
    transform: translateY(-7px);
}
.content-s2SEQO a,
.wrapper-3WhCwL { /*Description modal links*/
    color: var(--text-link);
}
.channelSettingButtons-23CIRg .button-18p_f6 { /*Edit channel buttons*/
    transition: filter 0.25s ease;
}
.channelSettingButtons-23CIRg .button-18p_f6:hover { /*Edit channel buttons hover*/
    background: transparent;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));    
}
.cozy-3raOZG.wrapper-2a6GCs.mentioned-xhSam7,
.cozy-3raOZG.wrapper-2a6GCs.replying-1x3H0T { /*Mentioned/Replying to message*/
    background-color: rgba(0, 0, 0, 0.05);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
    box-shadow: -2px -3px 5px 1px rgb(0, 0, 0);
    border-top-right-radius: var(--main-radius);
}
.cozy-3raOZG.wrapper-2a6GCs.mentioned-xhSam7::before,
.cozy-3raOZG.wrapper-2a6GCs.replying-1x3H0T::before { /*Mentioned/Replying to message vertical line*/
    background-color: rgb(var(--accent-color));
}
.modal-qgFCbT .imageWrapper-2p5ogY { /*Clicked image modal*/
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569);
}
.reaction-1hd86g { /*Message reactions*/
    border: none;
    background-color: transparent;
    transition: 0.25s ease;
}
.reaction-1hd86g:hover { /*Message reactions hovered*/
    border: none;
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.reaction-1hd86g.reactionMe-wv5HKu {/*Message reacted*/
    border: none;
    background-color: rgb(0, 0, 0, 0.35);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.container-3RCQyg { /*New channel message*/
    border-bottom: none;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.blockquoteDivider-2hH8H6 { /*Chat quote*/
    background-color: rgb(var(--server-channel-textc));
}
.jumpToPresentBar-G1R9s6 { /*Jump to present bar*/
    bottom: 0.95%;
    left: 50%;
    transform: translateX(-50%);
    height: 20px;
    width: 90%;
    background: var(--popout-bg);
    background-color: transparent;
    box-shadow: -3px -4px 6px 3px black, -3px -4px 6px 3px black, -3px -4px 6px 3px black;
    opacity: 1;
}
.jumpToPresentBar-G1R9s6 button,
.newMessagesBar-265mhP button { /*Jump to present/New messges text*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.newMessagesBar-265mhP { /*New messages bar*/
    width: 100%;
    background-color: transparent;
    backdrop-filter: blur(5px);
}
.autocomplete-1vrmpx { /*Autocomplete modal*/
    bottom: 105%;
    background: transparent;
    background-color: transparent!important;
    box-shadow: -3px -4px 6px 3px black;
    border-radius: var(--window-border-radius);
}
.autocomplete-1vrmpx::before { /*Autocomplete modal background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--window-border-radius);
    background: var(--popout-bg) center/cover no-repeat;
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.autocomplete-1vrmpx::after { /*Autocomplete modal opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--window-border-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.wrapper-uf3cnO,
.wrapper-2Gsate,
.wrapper-1-Fsb8,
.categoryHeader-O1zU94,
.bar-AokMp3 { /*Autocomplete subcontainers*/
    background-color: transparent;
}
.categoryHeader-O1zU94 { /*Category*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.categorySectionLast-2PPrHj .selectable-3dP3y- { /*Hovered autocompletion*/
    filter: opacity(0.35);
    transition: filter 0.25s ease;
}
.categorySectionLast-2PPrHj .selected-1Tbx07 { /*Selected autocompletion*/
    background-color: transparent;
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.wrapper-2siovq {
    color: rgb(var(--server-channel-textc));
    filter: opacity(0.35);
    transition: filter 0.25s ease;
}
.wrapper-2siovq:hover {
    background-color: transparent;
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.section-Kprrfe { /*Bot category hovered*/
    transition: filter 0.25s ease;
}
.section-Kprrfe:hover { /*Bot category hovered*/
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.section-Kprrfe foreignObject { /*Bot category hovered icon*/
    mask: none;
    border-radius: 50%;
}
.cozy-3raOZG .timestamp-3ZCmNB { /*Timestamps/Edited text*/
    color: rgb(var(--server-channel-textc));
}
.wrapper-39oAo3 { /*Follow chat container*/
    background-color: transparent;
}
.wrapper-39oAo3 .content-c_0cLD { /*Follow chat text*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.searchBar-3dMhjb { /*Search messages bar*/
    border: 2px solid rgba(var(--main-dark-color), 0.35);
    border-radius: var(--button-radius);
    background-color: transparent!important;
    transition: 0.25s ease;
    max-width: 180px;
}
.searchBar-3dMhjb:hover { /*Search messages bar*/
    border-color:  rgba(var(--main-dark-color), 0.65);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.searchBar-3dMhjb:focus-within { /*Search messages bar*/
    border-color:  rgba(var(--main-dark-color), 0.8);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.search-2oPWTC .DraftEditor-root .public-DraftEditorPlaceholder-root { /*Searchbar placeholder text*/
    color: rgba(var(--main-dark-color), 0.8);
    transition: 0.25s ease;
}
.search-2oPWTC:hover .DraftEditor-root .public-DraftEditorPlaceholder-root,
.search-2oPWTC:focus-within .DraftEditor-root .public-DraftEditorPlaceholder-root { /*Searchbar placeholder text*/
    color: rgba(var(--server-channel-textc), 1);
}
.container-3ayLPN { /*Search results modal*/
    border-radius: var(--main-radius);
    background-color: transparent!important;
    background: transparent;
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569)!important;
}
.container-3ayLPN::before { /*Search results modal*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background: var(--popout-bg) center/cover no-repeat;
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.container-3ayLPN::after { /*Search results modal*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.option-96V44q { /*Search results options*/
    filter: opacity(0.35);
    transition: 0.25s ease;
}
.option-96V44q.selected-rZcOL- { /*Search results hovered*/
    background-color: transparent!important;
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.option-96V44q:after { /*Gradient after option*/
    display: none;
}
.resultsGroup-r_nuzN:before { /*Divider*/
    display: none;
}
.resultsGroup-r_nuzN .header-2N-gMV, 
.resultsGroup-r_nuzN .plusIcon-v0BTrL, 
.resultsGroup-r_nuzN .searchClearHistory-2cSSMO, 
.resultsGroup-r_nuzN .searchLearnMore-3SQUAj a { /*Result options*/
    color: rgb(var(--server-channel-textc))!important;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.queryContainer-RKFJW- {
    background-color: transparent!important;
    color: rgb(var(--server-channel-textc))!important;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
    border-bottom: none;
}
.autocompleteRow-2OthDa .selected-1Tbx07 { /*Autocomplete items*/
    transition: 0.25s ease;
}
.autocompleteRow-2OthDa .selected-1Tbx07 { /*Autocomplete hovered*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
    background: transparent!important;
}
.divider-23swzi { /*Autocomplete divider*/
    display: none;
}
.contentTitle-2tG_sM { /*Matches*/
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.searchResultsWrap-3-pOjs {
    background-color: transparent;
    background: transparent;
}
.searchResultsWrap-3-pOjs::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background: var(--popout-bg) center/cover no-repeat;
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.searchResultsWrap-3-pOjs::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.searchHeader-2XoQg7,
.searchResult-9tQ1uo,
.channelName-1JRO3C {
    background-color: transparent;
}
.tab-2j5AEF {
    color: rgb(var(--server-channel-textc))!important;
    filter: opacity(0.35);
    transition: filter 0.25s ease;
}
.tab-2j5AEF:hover {
    background-color: transparent;
    color: rgb(var(--server-channel-textc))!important;
    filter: opacity(0.65) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.tab-2j5AEF.selected-2LAck8 {
    background-color: transparent!important;
    color: rgb(var(--server-channel-textc))!important;
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.totalResults--dyAxF,
.channelName-1JRO3C { /*Text*/
    color: rgb(var(--server-channel-textc))!important;
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.searchFilter-2ESiM3 { /*Search filter*/
    border-radius: var(--button-radius);
    background-color: rgba(var(--accent-color), 0.55)!important;
}
.searchAnswer-3Dz2-q { /*Search results*/
    background-color: transparent!important;
}
.pageButton-2ruNwd.activeButton-rvKcqq { /*Result pages selected*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
    color: rgb(var(--server-channel-textc))!important;
    background-color: transparent!important;
}
.pageButton-2ruNwd { /*Result pages*/
    transition: 0.25s ease;
    color: rgb(var(--server-channel-textc), 0.35)!important;
}
.pageButton-2ruNwd:hover { /*Result pages hovered*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
    color: rgb(var(--server-channel-textc), 0.65)!important;
    background-color: transparent!important;
}
.scroller-1-nKid,
.reactors-Blmlhw { /*Reactions modal*/
    background-color: transparent!important;
}
.reactorDefault-1IUqMZ { /*Dividers*/
    box-shadow: unset!important;
}
.replyBar-1YLQ2F,
.threadSuggestionBar-2ufK2Z,
.attachedBars-tZDmyV { /*Replying to bar*/
    background-color: transparent;
}

/*Pinned messages modal*/

.iconBadge-qZ4Ksk { /*Pinned messages icon*/
    background-color: rgb(var(--accent-color), .55);
}
@keyframes menuShow {
    0% {
        transform: scaleY(0);
    }
    100% {
        transform: scaleY(1);
    }
}

.messagesPopoutWrap-1MQ1bW { /*Main modal*/
    border-radius: var(--main-radius);
    background: transparent;
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569);
    max-height: 750px!important;
    animation: menuShow 0.25s ease;
    transform-origin: top;
}
.messagesPopoutWrap-1MQ1bW::before { /*Main modal background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background: var(--popout-bg) center/cover no-repeat;
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.messagesPopoutWrap-1MQ1bW::after { /*Main modal opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.messagesPopoutWrap-1MQ1bW .header-ykumBX { /*Header*/
    box-shadow: none;
    color: rgb(var(--server-channel-textc));
    text-align: center;
}
.header-ykumBX  .base-1x0h_U { /*Header text*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
    font-size: 1.15rem;
}
.header-ykumBX .base-1x0h_U::after { /*Header*/
    content: '';
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    bottom: -25%;
    height: 2px;
    width: 38%;
    background-color: rgb(var(--server-channel-textc));
}
.header-ykumBX,
.messageGroupWrapper-o-Zw7G { /*Subcointainers*/
    background-color: transparent;
    border: unset;
}
.jumpButton-3DTcS_,
.button-11zvza { /*Jump to message buton*/
    background-color: transparent;
    color: rgba(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.jumpButton-3DTcS_:hover,
.button-11zvza:hover { /*Jump to message buton*/
    color: rgba(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.footer-1kmXd4 { /*Pinned messages footer*/
    background-color: transparent;
}

/*Mentions settings*/

.header-2-Imhb .tab-ck0077 { /*Tab settings*/
    color: rgba(var(--server-channel-textc), 0.2);
    transition: 0.25s ease;
}
.header-2-Imhb .tabBar-1kuXvJ .tab-ck0077:hover { /*Hovered tab*/
    background-color: transparent!important;
    color: rgba(var(--server-channel-textc), 0.65);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.header-2-Imhb .tabBar-1kuXvJ .tab-ck0077.active-1MbGPa { /*Selected tab*/
    background-color: transparent!important;
    color: rgba(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.secondary-dIudih { /*Filter button*/
    color: rgba(var(--server-channel-textc), 0.35);
    background-color: transparent;
    transition: 0.25s ease;
}
.secondary-dIudih:hover:not(.disabled-3Njyym) { /*Filter button hovered*/
    background-color: transparent;
    color: rgba(var(--server-channel-textc), 0.65);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.channelHeader-3Gd2xq,
.messageContainer-gbhlwo { /*Mentions*/
    background-color: transparent;
}
.button-1-5Aqk { /*Close mention button*/
    background-color: transparent;
    color: rgb(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.tertiary-aMXF0g:hover:not(.disabled-3Njyym) { /*Close mention button hovered*/
    background-color: transparent;
    color: rgb(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.jumpButton-2dvRSC { /*Jump to message buton*/
    background-color: transparent;
    color: rgba(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.jumpButton-2dvRSC:hover { /*Jump to message buton*/
    color: rgba(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}

/*Inbox settings*/

.container-enaOkj { /*Main modal*/
    background: transparent;
    border-radius: var(--main-radius);
    background-color: transparent;
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569);
}
.container-enaOkj::before { /*Main modal background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background: var(--popout-bg) center/cover no-repeat;
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.container-enaOkj::after { /*Main modal opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.icon-1Itzco { /*No messges icon*/
    background-color: transparent;
}
.iconContainer-JbDkvn,
.container-enaOkj .header-2M8_sb,
.container-enaOkj .colorHeaderSecondary-3Sp3Ft { /*Empty messges text*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}


/*Button settings*/

.lookFilled-1Gx00P.colorGreen-29iAKY,
.lookFilled-1Gx00P.colorGrey-2DXtkV,
.lookFilled-1Gx00P.colorBrand-3pXr91,
.lookFilled-1Gx00P.colorRed-1TFJan,
.lookOutlined-3sRXeN.colorRed-1TFJan,
.lookOutlined-3sRXeN.colorBrand-3pXr91,
.lookInverted-2D7oAl.colorBrand-3pXr91,
.lookOutlined-3sRXeN.colorPrimary-3b3xI6,
.lookInverted-2D7oAl.colorGreen-29iAKY,
.buttonInvertedPurple-WtBglX,
.lookOutlined-3sRXeN.colorGreen-29iAKY { /*Buttons main settings*/
    border-radius: var(--button-radius);
    border: 1px solid;
    color: rgb(var(--server-channel-textc))!important;
    background-color: transparent;
    filter: opacity(0.35);
    transition: filter  0.25s ease;
}
.lookFilled-1Gx00P.colorGreen-29iAKY:hover,
.lookFilled-1Gx00P.colorGrey-2DXtkV:hover,
.lookFilled-1Gx00P.colorBrand-3pXr91:hover,
.lookFilled-1Gx00P.colorRed-1TFJan:hover,
.lookOutlined-3sRXeN.colorRed-1TFJan:hover,
.lookOutlined-3sRXeN.colorBrand-3pXr91:hover,
.lookInverted-2D7oAl.colorBrand-3pXr91:hover,
.lookOutlined-3sRXeN.colorPrimary-3b3xI6:hover,
.lookInverted-2D7oAl.colorGreen-29iAKY:hover,
.buttonInvertedPurple-WtBglX:hover,
.lookOutlined-3sRXeN.colorGreen-29iAKY:hover { /*Hovered buttons main settings*/
    background-color: transparent!important;
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.lookFilled-1Gx00P.colorPrimary-3b3xI6,
.lookFilled-1Gx00P.colorWhite-rEQuAQ  { /*Discord nitro gift grey button*/
    border-radius: var(--button-radius);
    border: 1px solid;
    color: rgb(var(--server-channel-textc))!important;
    background-color: transparent!important;
    filter: opacity(0.55);
    transition: filter  0.25s ease;
}
.lookFilled-1Gx00P.colorPrimary-3b3xI6:hover,
.lookFilled-1Gx00P.colorWhite-rEQuAQ:hover { /*Discord nitro gift grey button hovered*/
    background-color: transparent!important;
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.lookFilled-1Gx00P.colorRed-1TFJan,
.lookOutlined-3sRXeN.colorRed-1TFJan { /*Different red buttons*/
    border-color: red;
    color: red!important;
}
.lookFilled-1Gx00P.colorGrey-2DXtkV { /*Different grey buttons*/
    background-color: transparent!important;
    border-color: rgb(var(--server-channel-textc));
}
.lookLink-9FtZy-.colorPrimary-3b3xI6 .contents-18-Yxp { /*Cancel button*/
    color: rgb(var(--server-channel-textc))!important;
    filter: opacity(0.35);
    transition: filter  0.25s ease;
}
.lookLink-9FtZy-.colorPrimary-3b3xI6:hover .contents-18-Yxp:hover { /*Cancel button*/
    color: rgb(var(--server-channel-textc));
    background-image: none;
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.lookFilled-1Gx00P.colorBrand-3pXr91:disabled {
    background-color: transparent;
}
.title-3qD0b- .children-19S4PO .iconWrapper-2OrFZ1 .icon-22AiRD { /*Channel description icon*/
    color: rgb(var(--server-channel-textc));
}
.lookLink-9FtZy-.colorBrand-3pXr91 { /*No thanks button*/
    filter: opacity(0.35);
    transition: 0.25s ease;
}
.lookLink-9FtZy-.colorBrand-3pXr91:hover { /*No thanks button hovered*/
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.lookLink-9FtZy-.colorBrand-3pXr91:hover .contents-18-Yxp { /*No thanks button underline*/
    background: none;
}
.lookOutlined-3sRXeN.colorWhite-rEQuAQ { /*Activity buttons*/
    border-radius: var(--button-radius);
    color: rgb(var(--server-channel-textc), 0.65);
    border-color: rgb(var(--server-channel-textc), 0.65);
    transition: .25s ease;
}
.lookOutlined-3sRXeN.colorWhite-rEQuAQ:hover { /*Activity buttons*/
    color: rgb(var(--server-channel-textc), 1);
    border-color: rgb(var(--server-channel-textc), 1);
}
.lookOutlined-3sRXeN.colorWhite-rEQuAQ:disabled { /*Disabled activity button*/
    color: rgb(var(--server-channel-textc), 0.25);
    border-color: rgb(var(--server-channel-textc), 0.25);
}
.colorable-1bkp8v.primaryDark-3mSFDl { /*Raise hand button*/    
    background-color: transparent;
    color: rgb(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.colorable-1bkp8v.primaryDark-3mSFDl:hover { /*Raise hand button*/    
    background-color: transparent;
    color: rgb(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.button-1YfofB.buttonColor-7qQbGO.fauxDisabled-2ik0Vw, 
.button-1YfofB .buttonColor-7qQbGO.fauxDisabled-2ik0Vw, 
.button-1YfofB.buttonColor-7qQbGO:disabled, .button-1YfofB 
.buttonColor-7qQbGO:disabled { /*Disabled buttons*/
    background-color: transparent;
}
.title-3qD0b- .topic-TCb_qw { /*Channel description*/
    color: rgb(var(--server-channel-textc));
}
.title-3qD0b- .children-19S4PO { /*Top bar tooltip buttons*/
    transition: 0.25s ease;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.title-3qD0b-:hover .children-19S4PO { /*Top bar tooltip buttons hovered*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.content-1T5kuS+.footer-2gL1pp .button-38aScr .contents-18-Yxp { /*Can't find camera button*/
    color: rgb(var(--server-channel-textc), 1);
}
.button-1YfofB.buttonColor-7qQbGO.buttonActive-3FrkXp, 
.button-1YfofB .buttonColor-7qQbGO.buttonActive-3FrkXp { /*Streamming buttons*/
    background-color: transparent;
}
.upsellButton-1QHAmZ { /*Nitro buttons*/
    color: rgb(var(--server-channel-textc));
}

/*Message box*/

.channelTextArea-rNsIhG,
.scrollableContainer-2NUZem { /*Message box main containers*/
    background-color: transparent;
    border-radius: var(--main-radius);
}
.channelTextArea-rNsIhG { /*Message box width*/
    left: 50%;
    transform: translateX(-50%);
    width: 92.5%;
}
.scroller-2LSbBU { /*Messages scroller*/
    max-height: 99%;
}
.scrollableContainer-2NUZem::before { /*Message box background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    filter: brightness(0);
    background: transparent;
    box-shadow: 0px 0px 0px 0px black, 0px 0px 0px 0px black, 0px 0px 0px 0px black;
    transition: 0.25s ease;
    z-index: -1;
}
.scrollableContainer-2NUZem:focus-within::before { /*Message box background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    filter: brightness(0.15);
    box-shadow: -3px -4px 6px 3px black, -3px -4px 6px 3px black, -3px -4px 6px 3px black;
    transition: 0.35s ease;
    z-index: -1;
}
.container-2fRDfG { /*Replying to panel*/
    background-color: transparent;
}

/*Server channels settings*/

.header-2V-4Sw { /*Server name*/
    color: rgba(var(--server-channel-textc), 0.35);
    background-color: transparent;
    box-shadow: none;
    transition: filter 0.25s ease, color 0.25s ease;
}
.clickable-25tGDB:not(.selected-31Nl7x) .header-2V-4Sw:hover { /*Server name hover*/
    color: rgba(var(--server-channel-textc), 0.65);
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.selected-31Nl7x .header-2V-4Sw { /*Server name selected*/
    color: rgba(var(--server-channel-textc), 1);
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.selected-31Nl7x .header-2V-4Sw:hover { /*Hovered selected server*/
    background-color: transparent;
}
.containerDefault-3tr_sE { /*Channel categories*/
    padding-top: 10px;
}
.containerDefault-3tr_sE .wrapper-PY0fhH { /*Channel categories text*/
    width: fit-content;
    left: 50%;
    transform: translateX(-50%);
    max-width: 100%;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.containerDefault-3tr_sE .wrapper-PY0fhH .container-2ax-kl { /*Channel category text*/
    font-size: .85rem;
}
.mainContent-2h-GEV svg { /*Channel category collapsable arrow*/
    display: none;
}
.wrapper-2jXpOf .name-23GUGE { /*Channel name color*/
    color: rgb(var(--server-channel-textc))!important;
}
.wrapper-2jXpOf { /*channel names*/
    transition: filter 0.35s ease;
}
.wrapper-2jXpOf:not(.modeSelected-346R90):not(.modeUnread-1qO3K1) { /*Channel names*/
    filter: opacity(0.2);
}
.wrapper-2jXpOf:not(.modeSelected-346R90):hover { /*Channel names hovered*/
    filter: opacity(0.35) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.wrapper-2jXpOf.modeUnread-1qO3K1 { /*Channel name unread*/
    filter: opacity(0.45);
    transition: filter 0.35s ease;
}
.wrapper-2jXpOf.modeUnread-1qO3K1:hover { /*Channel name unread hovered*/
    filter: opacity(0.65) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.wrapper-2jXpOf.modeSelected-346R90 { /*Server selected channel text and icon*/
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
    transition: filter 0.35s ease;
}
.modeSelected-346R90 .content-1x5b-n { /*Server selected channel main container background*/
    background-color: transparent;
}
.containerDefault--pIXnN .unread-2lAfLh { /*Unread messages in channel background*/
    background-color: transparent;
}
.wrapper-2jXpOf:hover .content-1x5b-n { /*Server hovered channel main container background*/
    background-color: transparent;
}

@keyframes newUnreadChannel {
    0% {
        filter: opacity(0);
    }
    25% {
        filter: opacity(0.85);
    }
    50% {
        filter: opacity(0);
    }
    100% {
        filter: opacity(0.85);
    }
}
.mainContent-u_9PKf[aria-label*="unread,"] .iconContainer-1BBaeJ::before { /*Unread messages in channel glow*/
    content: '';
    position: absolute;
    top: 35%;
    left: 40%;
    width: 5px;
    height: 5px;
    background-color: rgba(var(--server-channel-textc), 0.4);
    box-shadow: 0px 0px 10px 3px rgb(var(--server-channel-textc)), 0px 0px 0px 0px inset rgb(var(--server-channel-textc));
    animation: newUnreadChannel 1s ease;
    animation-fill-mode: forwards;
}
.audienceVoiceUserIconContainer-29oflP { /*Audience in channel icon*/
    background-color: transparent;
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.audienceVoiceUserText-BhGzmw { /*Audience in channel*/
    color: rgb(var(--server-channel-textc));
}
.listDefault-3ir5aS .clickable-1lCRLF .content-1Wq3SX .username-3KYl0N { /*People in channel name*/
    color: rgba(var(--server-channel-textc), 0.35)!important;
    transition: 0.25s ease;
}
.listDefault-3ir5aS .clickable-1lCRLF:hover .content-1Wq3SX .username-3KYl0N { /*People in channel name hovered*/
    color: rgba(var(--server-channel-textc), 0.65)!important;
}
.listDefault-3ir5aS .clickable-1lCRLF.selected-3t3Csj .content-1Wq3SX .username-3KYl0N  { /*Selecter user in channel name*/
    color: rgba(var(--server-channel-textc), 1)!important;
}
.listDefault-3ir5aS .clickable-1lCRLF .content-1Wq3SX { /*User in channel*/
    transition: 0.25s ease;
}
.listDefault-3ir5aS .clickable-1lCRLF:hover .content-1Wq3SX { /*User in channel shadow*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.listDefault-3ir5aS .clickable-1lCRLF.selected-3t3Csj .content-1Wq3SX { /*Selected user in channel bg*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.channelNotice-2bJINM { /*Channel notice*/
    border-bottom: none;
}
.channelNotice-2bJINM > .textBlock-2FWDjE,
.channelNotice-2bJINM .eventName-2YgbEu { /*Channel notice text*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.subtitle-3V1p2E { /*Channel subtitle*/
    color: rgb(var(--server-channel-textc));
}
.unread-1xRYoj { /*Unreads*/
    background: transparent;
    opacity: 1;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.unread-1xRYoj::before { /*Unreads background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background: var(--popout-bg) center/cover no-repeat;
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.unread-1xRYoj::after { /*Unreads opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.unread-1xRYoj .text-2e2ZyG { /*Unread text*/
    color: rgba(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}

/*Server members*/

.members-1998pB>div, 
.container-2wlB3z { /*Server members panel background*/
    background-color: transparent;
}
.membersWrap-2h-GB4 { /*Main modal*/
    margin-bottom: 22px;
}
.membersGroup-v9BXpm { /*Server roles*/
    text-align: center;
    color: rgb(var(--server-channel-textc));
}
.membersGroup-v9BXpm span { /*Server roles title*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
    font-size: 0.85rem;
}
.member-3-YXUe .layout-2DM8Md,
.member-3-YXUe { /*Server member container*/
    transition: filter 0.25s ease;
}
.member-3-YXUe:hover .layout-2DM8Md { /*Server member container*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.member-3-YXUe.selected-aXhQR6 { /*Selected member*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.member-3-YXUe.selected-aXhQR6 .layout-2DM8Md { /*Selected member*/
    background-color: transparent;
}
.member-3-YXUe .activityText-yGKsKm { /*Server member activity*/
    color: rgb(var(--server-channel-textc));
}
.botTagRegular-2HEhHi,
.botTagInvert-18-95s { /*Bot tag*/
    background-color: transparent;
    color: rgb(var(--accent-color), .55);
}

/*Nitro page*/

.applicationStore-1pNvnv,
.scroller-9moviB {
    background-color: transparent;
}

/*User status area*/

.panels-j1Uci_ { /*Main panel*/
    background-color: transparent;
}
.container-3baos1 { /*Subcontainer*/
    margin-bottom: 22px;
}
.container-3baos1 .button-14-BFJ { /*Mute/Deafen/Settings buttons*/
    color: rgb(var(--server-channel-textc));
    filter: opacity(0.2);
    transition: 0.25s ease;
}
.container-3baos1 .button-14-BFJ:hover { /*Mute/Deafen/Settings buttons*/
    filter: opacity(0.65) drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
    background-color: transparent;
}
.container-3baos1 .button-14-BFJ[aria-checked='true'] { /*Mute/Deafen/Settings buttons checked*/
    filter: opacity(1) drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.container-3baos1 .button-14-BFJ .strikethrough-1n4ekb { /*Mute/Deafen strikethrough*/
    color: rgb(var(--accent-color));
}
.container-1giJp5,
.activityPanel-28dQGo,
.listeningAlong-30wH70 { /*Connected to server / User activity*/
    border-bottom: none;
}
.connection-3KRENF,
.voiceUsers-YsH5Db,
.activityPanel-28dQGo,
.listeningAlong-30wH70 { /*Connected to server text*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.button-14-BFJ { /*Buttons*/
    color: rgba(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.button-14-BFJ.enabled-2cQ-u7:hover { /*Buttons hovered*/
    background-color: transparent;
    color: rgba(var(--server-channel-textc), 1);
}

#status-picker.menu-3sdvDG { /*Select status menu*/
    transform-origin: bottom;
}

/*Go live panel*/

.segmentControlOption-1vCKaY { /*Go live tabs*/
    color: rgb(var(--server-channel-textc), 0.35);
    border-color: rgb(var(--server-channel-textc), 0.35)!important;
    transition: 0.25s ease;
}
.segmentControlOption-1vCKaY:hover { /*Tabs hovered*/
    color: rgb(var(--server-channel-textc), 0.65);
    border-color: rgb(var(--server-channel-textc), 0.65)!important;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.segmentControlOption-1vCKaY.selected-P8xTeN { /*Selected tab*/
    color: rgb(var(--server-channel-textc), 1);
    border-color: rgb(var(--server-channel-textc), 1)!important;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.card-2Mz_4z { /*Streaming info*/
    color: rgb(var(--server-channel-textc));
    background-color: transparent;
    border: none;
}
.qualitySettingsContainer-1gOtRJ { /*Quality container*/
    border: none;
}
.lookFilled-22uAsw.select-2fjwPw { /*Dropdown menu*/
    border-radius: var(--main-radius);
    background-color: transparent;
    border: none;
}
.popout-VcNcHB { /*Dropdown options*/
    background-color: transparent;
    border: none;
}
.popout-VcNcHB::before { /*Dropdown options background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--popout-bg) center/cover no-repeat;
    border-bottom-left-radius: var(--main-radius);
    border-bottom-right-radius: var(--main-radius);
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.popout-VcNcHB::after { /*Dropdown options opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-bottom-left-radius: var(--main-radius);
    border-bottom-right-radius: var(--main-radius);
    background-color: rgba(0,0,0, 0.4);
    z-index: -1;
}
.option-3KoAJB { /*Options*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) opacity(0.35);
    color: rgb(var(--server-channel-textc));
    background-color: transparent!important;
    transition: 0.25s ease;
}
.option-3KoAJB:hover { /*Option hovered*/
    color: rgb(var(--server-channel-textc));
    filter: opacity(0.65);
}
.option-3KoAJB[aria-selected=true],
.selectedIcon-3uS11H { /*Selected option*/
    filter: opacity(1);
    color: rgb(var(--accent-color));
}
.headerText-2j81og,
.headerDescription--F5XUT,
.formItemTitle-155OC0 { /*Text*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.item-3T2z1R .colorStandard-2KCXvj { /*Quality text*/
    color: rgba(var(--server-channel-textc), 0.35)!important;
    transition: 0.25s ease;
}
.item-3T2z1R { /*Quality buttons*/
    background: transparent;
    transition: 0.25s ease;
    border: none;
}
.item-3T2z1R:hover { /*Hovered quaility button*/
    background-color: transparent!important;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.item-3T2z1R:not(.selectorButtonSelected-t5V9On):hover .colorStandard-2KCXvj { /*Hovered quality text*/
    color: rgba(var(--server-channel-textc), 0.65)!important;
}
.item-3T2z1R.selectorButtonSelected-t5V9On { /*Selected quality button*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.item-3T2z1R.selectorButtonSelected-t5V9On .colorStandard-2KCXvj { /*Selected quality text*/
    color: rgba(var(--server-channel-textc), 1)!important;
}
.wrapper-2qzCYF { /*Streaming window | Call window*/
    background-color: transparent;
    
}
.wrapper-2qzCYF .children-19S4PO > div,
.wrapper-2qzCYF .children-19S4PO h3 { /*Channel name*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.wrapper-2qzCYF .container-1r6BKw.transparent-2ZlE3R .controlIcon-35oS15 {
    color: rgb(var(--server-channel-textc), 0.65);
    transition: 0.25s ease;
}
.wrapper-2qzCYF .container-1r6BKw.transparent-2ZlE3R .controlIcon-35oS15:hover { /*Toolbar buttons*/
    color: rgb(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.wrapper-2qzCYF  .listItems-1uJgMC,
.bottomControls-lIJyYL { /*Shadows*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.colorable-1bkp8v.white-3GPOIp,
.colorable-1bkp8v.white-3GPOIp.active-1QRrIS,
.colorable-1bkp8v.red-33-Lnk,
.colorable-1bkp8v.red-33-Lnk.active-1QRrIS,
.colorable-1bkp8v.red-33-Lnk:hover { /*Go live buttons*/
    filter: opacity(0.25);
    background-color: transparent;
    transition: 0.25s ease;
}
.colorable-1bkp8v.white-3GPOIp:hover,
.colorable-1bkp8v.red-33-Lnk:hover {
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.colorable-1bkp8v.white-3GPOIp .centerIcon-2G6o-T,
.contextMenuCaret-3tjo32,
.colorable-1bkp8v.primaryDark-3mSFDl .centerIcon-2G6o-T { /*Go live buttons icons*/
    color: rgb(var(--server-channel-textc), 1);
}
.colorable-1bkp8v.red-33-Lnk,
.colorable-1bkp8v.red-33-Lnk .centerIcon-2G6o-T { /*End call*/
    color: red;
}
.tile-2naSqK,
.button-3HqqDX,
.button-3HqqDX:hover { /*No one's here*/
    background-color: transparent;
}
.divider-T9ghJP { /*Divider*/
    display: none;
}

/*User card*/

.userPopout-xaxa6l { /*Main modal*/
    border-radius: var(--main-radius);
    background: transparent;
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569);
}
.userPopout-xaxa6l::before { /*Main modal background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background: var(--popout-bg) center/cover no-repeat;
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.userPopout-xaxa6l::after { /*Main modal opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.userPopout-xaxa6l .headerNormal-3KXFBt { /*User card header*/
    background-color: transparent!important;
}
.avatarWrapper-3r9PdD,
.headerTop-3vNv-a,
.aboutMeSection-1Fw5Ia { /*Avatar, username and about me*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.headerTagUsernameNoNickname-2-Y5Ct { /*Username*/
    color: rgb(var(--server-channel-textc));
}
.userPopout-xaxa6l .body-3HBlXn,
.footer-3UKYOU { /*User card body/footer*/
    background-color: transparent!important;
}
.body-3HBlXn { /*Body padding*/
    padding-bottom: 3px;
}
.role-2irmRk { /*User card roles*/
    border-radius: var(--button-radius);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
    margin-right: 6px;
    background: transparent;
    border-color: transparent!important;
}
.bodyInnerWrapper-26fQXj { /*User card body subtitles container*/
    text-align: center;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
    background-color: transparent;
}
.bodyTitle-1ySSKn,
.aboutMeTitle-1IYtPE { /*User card body subtitles*/
    width: fit-content;
    border-bottom: 1px solid rgb(var(--server-channel-textc));
    color: rgb(var(--server-channel-textc));
}
.note-1MiCN7 { /*User card note*/
    height: fit-content;
    margin-left: 0px;
    margin-right: 0px;
    width: 99.085%;
    height: 50%;
}
.textarea-2r0oV8 { /*User card note text area*/
    height: fit-content;
    width: 100.93%!important;
    height: 50%!important;
    background-color: transparent!important;
}
.input-cIJ7To { /*Message user*/
    border-color: rgba(var(--server-channel-textc), .35);
    border-radius: var(--button-radius);
    transition: 0.25s ease;
}
.input-cIJ7To:hover { /*Message user hover*/
    border-color: rgba(var(--server-channel-textc), 0.65);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.input-cIJ7To:focus { /*Message user focus*/
    border-color: rgba(var(--server-channel-textc), 1)!important;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.activity-11LB_k { /*User card activity*/
    background-color: transparent;
}
.headerTop-2cWpdB { /*New header top*/
    background-color: transparent;
    border: none;
}
.input-2_SIlA { /*Message box input*/
    background-color: transparent;
}
.avatar-37jOim { /*User card avatar*/
    top: 6px;
    left: 6px;
    border: none;
    background-color: transparent;
}
.aboutMeSection-3bipSD,
.aboutMeSection---MkQa { /*About me*/
    background-color: transparent;
}
.aboutMeTitle-2M2L3- { /*About me title*/
    width: fit-content;
    color: rgb(var(--server-channel-textc))!important;
    border-bottom: 1px solid rgb(var(--server-channel-textc));
}
.betaBadge-1Ve-yb,
.betaBadge-2EDLLs { /*Beta Badge*/
    background-color: transparent!important;
    color: rgb(var(--accent-color));
}
.divider-ewBQKj { /*User card divider*/
    background-color: transparent;
}

/*Profile modal*/

.root-3QyAh1 { /*Main modal*/
    border-radius: var(--main-radius);
    background: transparent;
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569);
    background-color: transparent;
}
.root-3QyAh1::before { /*Main modal background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background: var(--popout-bg) center/cover no-repeat;
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.root-3QyAh1::after { /*Main modal opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.topSection-y3p-_D, 
.body-r6_QPy { /*Subcontainers*/
    background-color: transparent!important;
}
.tabBarContainer-37hZsr,
.userInfoSection-q_35fn+.userInfoSection-q_35fn,
.noTabBar-3ZjPNR { /*Profile divider*/
    border: none;
}
.thin-1ybCId::-webkit-scrollbar-thumb { /*Profile scrollbar*/
    background-color: rgb(var(--server-channel-textc))!important;
}
.topSectionNormal-2-vo2m .avatar-3EQepX,
.topSectionNormal-2-vo2m .headerInfo-30uryT { /*User info*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.activity-1ythUs,
.userInfoSectionHeader-CBvMDh { /*Subtitles*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.topSectionNormal-2-vo2m .additionalActionsIcon-1FoUlE { /*Three dots*/
    color: rgb(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.topSectionNormal-2-vo2m .additionalActionsIcon-1FoUlE:hover { /*Three dots hovered*/
    color: rgb(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.tabBar-3nvOPa { /*Profile tabs main*/
    height: 25px;
}
.top-28JiJ- .item-PXvHYJ { /*Profile tabs*/
    color: rgb(var(--server-channel-textc), 0.35);
    border-color: rgb(var(--server-channel-textc), 0.35)!important;
    transition: 0.25s ease;
    margin-right: 20px;
}
.top-28JiJ- .item-PXvHYJ:hover { /*Profile tabs*/
    color: rgb(var(--server-channel-textc), 0.65);
    border-color: rgb(var(--server-channel-textc), 0.65)!important;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.top-28JiJ- .selected-3s45Ha.item-PXvHYJ,
.top-28JiJ- .item-PXvHYJ[style="border-color: rgb(255, 255, 255); color: rgb(255, 255, 255);"] { /*Selected tab*/
    color: rgb(var(--server-channel-textc), 1)!important;
    border-color: rgb(var(--server-channel-textc), 1)!important;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.connectedAccount-2Jb-Z0 { /*Connected account*/
    border-radius: var(--button-radius);
    border-color: rgb(var(--server-channel-textc), 0.15);
    transition: 0.25s ease;
}
.connectedAccountName-E1KzaT,
.connectedAccountOpenIcon-2cNbq5 { /*Connected account text and icon*/
    color: rgb(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.connectedAccount-2Jb-Z0:hover { /*Connected account hover*/
    border-color: rgb(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.connectedAccount-2Jb-Z0:hover .connectedAccountName-E1KzaT,
.connectedAccount-2Jb-Z0:hover .connectedAccountOpenIcon-2cNbq5 { /*Connected account text and icon hovered*/
    color: rgb(var(--server-channel-textc), 1);
}
.listRow-1iDGel { /*Shared servers*/
    transition: 0.25s;
}
.listRow-1iDGel .listRowContent-3Kih4Q { /*Shared servers text*/
    color: rgb(var(--server-channel-textc), 0.35);
}
.listRow-1iDGel:hover .listRowContent-3Kih4Q { /*Shared servers*/
    color: rgb(var(--server-channel-textc), 1);
}
.listRow-1iDGel:hover { /*Shared servers hover*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black);
}
.topSectionPlaying-1J5E4n,
.headerFill-39azRn,
.topSectionSpotify-1lI0-P,
.topSectionStreaming-1Tpf5X { /*Profile activities*/
    background-color: transparent;
}
.avatar-AvHqJA { /*Profile avatar*/
    background-color: transparent;
    border: none;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}

/*Upload file modal*/

.uploadModal-2ifh8j { /*Main modal*/
    background-color: transparent!important;
    border-radius: var(--main-radius);
    box-shadow: -3px -6px 10px 10px black!important;
}
.uploadModal-2ifh8j::before { /*Main modal background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background: var(--popout-bg) center/cover no-repeat;
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.uploadModal-2ifh8j::after { /*Main modal opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.uploadModal-2ifh8j .footer-3mqk7D { /*Footer*/
    background-color: transparent!important;
    box-shadow: unset!important;
}
.uploadModal-2ifh8j .inner-3nWsbo .file-34mY5K .icon-kyxXVr.image-2yrs5j { /*Image preview*/
    background-color: transparent;
    box-shadow: unset;
    filter: drop-shadow(-3px -1px 3px black);
}
.checkboxWrapper-SkhIWG { /*Checkbox*/
    color: rgb(var(--server-channel-textc));
    transition: filter 0.35s ease;
}
.checkboxWrapper-SkhIWG:hover:not(.checked-3_4uQ9),
.checkboxWrapper-SkhIWG .checked-3_4uQ9 { /*Checkbox hovered*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.checkboxWrapper-SkhIWG .checked-3_4uQ9 { /*Checkbox box checked*/
    border-color: rgb(var(--server-channel-textc))!important;
}
.checkboxWrapper-SkhIWG .checked-3_4uQ9 svg path{ /*Checkbox box checked svg*/
    fill: rgb(var(--server-channel-textc));
    transition: fill 0.35s ease;
}

/*Friends Window*/

.peopleList-3c4jOR .title-30qZAO { /*Friends status title*/
    text-align: center;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
    font-size: 0.85rem;
    grid-area: header;
}
.container-1D34oG .toolbar-1t6TWx, /*Inbox, help, etc container*/
.headerBarContainer-31FKNA .toolbar-1t6TWx { /*Stage modal toolbar*/
    position: absolute;
    right: 8.506%;
    transform: translateX(-8.506%);
}
.tabBody-3YRQ8W:before { /*Box shadow after Online, All, etc buttons*/
    box-shadow: none;
}
.peopleList-3c4jOR { /*Main friends modal*/
    margin: 0 20px 0 20px;
}
.peopleList-3c4jOR > div { /*Grid*/
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    column-gap: 15px;
    row-gap: 10px;
    grid-template-areas: "header header header";
    padding: 0 10px 0 10px;
}
.peopleList-3c4jOR .title-30qZAO { /*Online friends etc position*/
    grid-area: header;
}
.peopleListItem-2nzedh { /*Friends main container*/
    border-top: none;
    height: 125px!important;
    border-radius: 8px;
    border: 1.5px solid rgba(var(--server-channel-textc), 0.55);
    margin-left: 0;
    margin-right: 0;
    transition: .25s ease;
}
.peopleListItem-2nzedh:hover,
.peopleListItem-2nzedh.active-rhSpJJ { /*Friends main container hovered/active*/
    margin: unset;
    padding: unset;
    background-color: transparent;
    border: 2px solid rgba(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.peopleListItem-2nzedh.active-rhSpJJ+.peopleListItem-2nzedh, 
.peopleListItem-2nzedh:hover+.peopleListItem-2nzedh { /*Card after selected/hovered one*/
    border-color: rgba(var(--server-channel-textc), 0.55);
}
.peopleListItem-2nzedh .actions-1SQwjn .actionButton-uPB8Fs,
.peopleListItem-2nzedh .userInfo-2zN2z8 { /*Friend card info transition*/
    transition: 0.25s ease;
}
.peopleListItem-2nzedh .userInfo-2zN2z8 { /*Friend card info*/
    margin-left: 5px;
    max-width: 230px;
}
.peopleListItem-2nzedh:hover .userInfo-2zN2z8 { /*Friend card info*/
    margin-left: 5px;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.peopleListItem-2nzedh .actions-1SQwjn { /*Friend card buttons*/
    margin-right: 5px;
}
.peopleListItem-2nzedh .actions-1SQwjn .actionButton-uPB8Fs,
.peopleListItem-2nzedh:hover .actions-1SQwjn .actionButton-uPB8Fs { /*Friend card buttons container*/
    background-color: transparent;
}
.peopleListItem-2nzedh:hover .actions-1SQwjn .actionButton-uPB8Fs { /*Friend card buttons container*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.content-98HsJk .container-1D34oG .children-19S4PO > .iconWrapper-2OrFZ1 .icon-22AiRD,
.content-98HsJk .container-1D34oG .base-1x0h_U { /*Friends text/icon*/
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.content-98HsJk .children-19S4PO .tabBar-ZmDY9v .item-3HknzM { /*Friends status tab*/
    color: rgba(var(--server-channel-textc), 1);
    transition: 0.25s ease;
}
.content-98HsJk .children-19S4PO .tabBar-ZmDY9v .item-3HknzM:hover { /*Friends status tab hovered*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.content-98HsJk .children-19S4PO .tabBar-ZmDY9v .selected-3s45Ha.item-3HknzM { /*Friends status tab selected*/
    border-bottom: 3px solid rgb(var(--server-channel-textc));
    border-radius: 0px;
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.topPill-30KHOu .item-PXvHYJ[aria-controls="add_friend-tab"] { /*Add friend tab*/
    color: rgba(var(--server-channel-textc), 1)!important;
    background-color: transparent!important;
    transition: 0.25s ease;
}
.topPill-30KHOu .item-PXvHYJ[aria-controls="add_friend-tab"]:hover { /*Add friend tab hovered */
    color: rgba(var(--server-channel-textc), 1)!important;
    background-color: transparent!important;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.topPill-30KHOu .item-PXvHYJ[aria-controls="add_friend-tab"][aria-selected="true"] { /*Add friend tab selected*/
    color: rgba(var(--server-channel-textc), 1)!important;
    border-radius: 0px;
    border-bottom: 3px solid rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.sectionHeader-20RGqu { /*Add friends window line*/
    border-color: transparent!important;
}
.wrapper-1cBijl { /*Add friend username input*/
    background-color: transparent;
    border-radius: var(--button-radius);
    border-color: rgba(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.wrapper-1cBijl:hover { /*Add friend username input hovered*/
    border-color: rgba(var(--server-channel-textc), 0.65);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.wrapper-1cBijl .lookFilled-1Gx00P.colorBrand-3pXr91 {
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
    transition: 0.25s ease;
}
.wrapper-1cBijl:focus-within { /*Add friend username input focused*/
    border-color: rgba(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.addFriendInput-4bcerK, 
.addFriendInput-4bcerK::placeholder { /*Add friend text*/
    color: rgb(var(--server-channel-textc));
}
.actionButton-uPB8Fs,
.actionButton-uPB8Fs.highlight-Lf97TE { /*Blocked button*/
    background-color: transparent;
}
.wrapper-2qzCYF.minimum-28Z35l { 
    background-color: transparent;
}
.newBrand .hero-EvfTTA { /*Nitro banner*/
    background-image: url();
}

/*DM panel*/

.searchBar-6Kv8R2 { /*DM Searchbar*/
    box-shadow: none;
}
.privateChannels-1nO12o .searchBar-6Kv8R2 .searchBarComponent-32dTOx { /*DM searchbar*/
    background-color: transparent;
    color: rgb(var(--server-channel-textc), 1);
}
.privateChannels-1nO12o .searchBar-6Kv8R2 { /*DM searchbar*/
    border: 2px solid rgba(var(--server-channel-textc), 0.35);
    border-radius: var(--button-radius);
    height: fit-content;
    margin-top: 10px;
    transition: 0.25s ease;
}
.privateChannelsHeaderContainer-3NB1K1 { /*Direct message header*/
    filter: opacity(0.2);
    color: rgb(var(--server-channel-textc));
    transition: 0.25s ease;
}
.privateChannelsHeaderContainer-3NB1K1:hover { /*Direct message header*/
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));;
    color: rgb(var(--server-channel-textc));
}
.privateChannels-1nO12o .searchBar-6Kv8R2:hover { /*DM searchbar*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.privateChannels-1nO12o .container-2Pjhx- .content-3QAtGj,
.privateChannels-1nO12o .container-2Pjhx- .linkButtonIcon-Mlm5d6 { /*DM channel*/
    filter: opacity(0.2);
    color: rgb(var(--server-channel-textc));
}
.privateChannels-1nO12o .container-2Pjhx- .avatar-3uk_u9,
.privateChannels-1nO12o .container-2Pjhx- .content-3QAtGj,
.privateChannels-1nO12o .container-2Pjhx- .linkButtonIcon-Mlm5d6 { /*DM channel subcontainer*/
    transition: 0.35s ease;
}
.privateChannels-1nO12o .container-2Pjhx-:not(.selected-aXhQR6):hover .content-3QAtGj { /*DM channel hovered name*/
    filter: opacity(0.65) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
    color: rgb(var(--server-channel-textc));
}
.privateChannels-1nO12o .container-2Pjhx-:not(.selected-aXhQR6):hover .avatar-3uk_u9 { /*DM channel hovered name*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.privateChannels-1nO12o .container-2Pjhx-:hover .linkButtonIcon-Mlm5d6 { /*DM channel icons hovered*/
    filter: opacity(0.65);
}
.privateChannels-1nO12o .container-2Pjhx-.selected-aXhQR6 .content-3QAtGj { /*DM channel selected*/
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
    color: rgb(var(--server-channel-textc));
}
.privateChannels-1nO12o .container-2Pjhx-.selected-aXhQR6 .avatar-3uk_u9 { /*DM channel hovered name*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.privateChannels-1nO12o .container-2Pjhx-.selected-aXhQR6 .linkButtonIcon-Mlm5d6 { /*DM channel icons selected*/
    filter: opacity(1);
}
.privateChannels-1nO12o .selected-aXhQR6 .layout-2DM8Md,
.privateChannels-1nO12o .container-2Pjhx-:not(.selected-aXhQR6):hover .layout-2DM8Md { /*DM channel selected/hovered background*/
    background-color: transparent;
}
.quickswitcher-3JagVE { /*Ctrl+K modal*/
    background-color: transparent;
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569);
}
.quickswitcher-3JagVE::before { /*Ctrl+K modal background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background: var(--popout-bg) center/cover no-repeat;
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.quickswitcher-3JagVE::after { /*Ctrl+K modal opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.input-2VB9rf { /*Ctrl+K modal searchbar*/
    background-color: transparent;
    box-shadow: none;
    border: 1px solid rgba(var(--server-channel-textc), 0.35);
    border-radius: var(--button-radius);
    transition: 0.25s ease;
}
.input-2VB9rf:hover { /*Ctrl+K modal searchbar hovered*/
    border-color: rgba(var(--server-channel-textc), 0.65);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.input-2VB9rf:focus-within { /*Ctrl+K modal searchbar focused*/
    border-color: rgba(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
}
.scroller-zPkAnE { /*Ctrl+K modal footer*/
    background-color: transparent;
}
.scroller-zPkAnE .contentDefault-16dKSY { /*Ctrl+K result*/
    color: rgb(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.scroller-zPkAnE .contentUnread-3gTHvA { /*Ctrl+K result unread*/
    color: rgb(var(--server-channel-textc), 0.65);
}
.scroller-zPkAnE .resultFocused-3aIoYe .contentDefault-16dKSY,
.scroller-zPkAnE .resultFocused-3aIoYe .contentUnread-3gTHvA { /*Ctrl+K result hovered text*/
    color: rgb(var(--server-channel-textc), 1);
}
.scroller-zPkAnE .resultFocused-3aIoYe { /*Ctrl+K result hovered*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-2px 0px 1px rgb(0, 0, 0));
    transition: 0.25s ease;
}
.scroller-zPkAnE .content-3YMskv div[style="height: 15px;"] {
    height: 0px!important;
}
.scroller-zPkAnE::-webkit-scrollbar-track { /*Ctrl+K scrollbar*/
    background-color: transparent!important;
}

/*Active Now*/

.container-lRFx4q { /*Main container*/
    background-color: transparent;
}
.nowPlayingColumn-2sl4cE .header-2SF4Nh,
.nowPlayingSidebar-2OFn0o .header-2SF4Nh { /*Active now text*/
    text-align: center;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
    font-size: 0.9rem;
    padding-bottom: 0px;
    margin-top: -4px;
    font-weight: 600;
}
.nowPlayingColumn-2sl4cE .wrapper-3D2qGf,
.nowPlayingSidebar-2OFn0o .wrapper-3D2qGf { /*Active now cards main container*/
    margin-bottom: 18px;
}
.itemCard-v9viV7 { /*Active now cards*/
    border-radius: 8px;
    background: var(--popout-bg) center/cover no-repeat;
    box-shadow: 0px 0px 0px 0px rgba(0, 0, 0, 0.569);
    border: unset;
    transition: box-shadow .25s ease;
}
.itemCard-v9viV7 .inset-3sAvek { /*Active now activity*/
    background-color: transparent!important;
}
.itemCard-v9viV7:hover { /*Active now cards*/
    box-shadow: -3px -3px 5px 3px rgba(0, 0, 0, 0.569);
}
.emptyCard-1RJw8n {
    background-color: transparent;
}
.nowPlayingColumn-2sl4cE .wrapper-3D2qGf > div,
.nowPlayingSidebar-2OFn0o .wrapper-3D2qGf > div  { /*Active now card info*/
    transition: filter 0.25s ease;
}
.nowPlayingColumn-2sl4cE .wrapper-3D2qGf:hover > div,
.nowPlayingSidebar-2OFn0o .wrapper-3D2qGf:hover > div { /*Active now hovered card info*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.nowPlayingColumn-2sl4cE .emptyText-2zjpZr,
.nowPlayingSidebar-2OFn0o .emptyText-2zjpZr { /*No one active text*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.voiceSectionDetails-2DQTfs:hover .voiceSectionText-vrWR1s { /*Hovered activity*/
    text-decoration: none;
}
.voiceSectionIconWrapper-FO7UEY { /*Voice chanel icon*/
    background-color: transparent!important;
}
.section-2gLsgF { /*Activity*/
    background-color: transparent;
}
.separator-XqIyoz { /*Divider*/
    display: none;
}
.partyMemberOverflow-lXnzvu { /*Party members*/
    background-color: transparent;
}
.scroller-2ZPeAD { /*active now border*/
    border: none;
}

/*Guilds*/

.childWrapper-anI2G9,
.wrapper-1BJsBx.selected-bZ3Lue .childWrapper-anI2G9,
.wrapper-1BJsBx:hover .childWrapper-anI2G9 { /*Home icon background color*/
    background: transparent;
}
.homeIcon-FuNwkv { /*Changes the home icon*/
    color: transparent !important;
    background: var(--home-icon-image) center/cover no-repeat;
    z-index: 2;
    width: 56px;
    height: 56px;
    transition: filter 0.25s ease;
}
.homeIcon-FuNwkv:hover { /*Hovered home icon*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.tree-2wKJdG:focus { /*Removes outline when double clicking guild bar*/
    outline: none;
}
.blobContainer-pmnxKB .wrapper-25eVIn foreignObject { /*Guild icon mask*/
    mask: none;
    border-radius: 50%;
    transition: filter 0.25s ease;
}
.listItem-GuPuDH .pill-1z4sAY {
    overflow: visible!important;
}
.blobContainer-pmnxKB .wrapper-25eVIn:hover foreignObject { /*Guild icon mask*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.folder-1hbNCn { /*Folder settings*/
    background-color: transparent;
    transition: filter 0.25s ease;
}
.folder-1hbNCn:hover { /*Folder settings hovered*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.folderIconWrapper-1_bOZe { /*Folder background*/
    background-color: transparent!important;
}
.circleIconButton-1QV--U { /*Add/Explore servers*/
    background-color: transparent;
    color: rgba(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.circleIconButton-1QV--U:hover { /*Add/Explore servers hovered*/
    background-color: transparent;
    color: rgba(var(--server-channel-textc), .55);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.circleIconButton-1QV--U.selected-1JjBPm { /*Add/Explore servers selected*/
    background-color: transparent;
    color: rgba(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.pill-3N7f9r { /*Server hovered element*/
    overflow: visible!important;
}
.item-2hkk8m { /*Server hovered*/
    background-color: rgb(var(--server-channel-textc));
    width: 4px;
    border-radius: 0px;
    margin-left: 0px;
    transform: translateX(2px)!important;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.expandedFolderBackground-1cujaW { /*Expanded folder background*/   
    background-color: transparent;
}
.upperBadge-2XnnGB,
.lowerBadge-29hYVK { /*Badges*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.iconBadge-3qSJIw.participating-1NvRVd { /*Participating badge*/
    background-color: rgb(var(--accent-color), 0.55);
}
.numberBadge-2s8kKX { /*Number badge*/
    background-color: rgb(var(--accent-color), .55)!important;
}

/*Explore servers*/

.pageWrapper-1PgVDX { /*Main modal*/
    background-color: transparent!important;
    height: 98%;
}
.headerImage-3X1tyY { /*Explore servers banner*/
    display: none;
}
.searchBox-3Y2Vi7 { /*Explore servers searchbar*/
    background-color: transparent!important;
    box-shadow: unset!important;
}
.search-1iTphC .searchBox-2_mAlO,
.input--jS-j2 { /*Explore servers searchbar subcontainer*/
    background-color: transparent;
}
.search-1iTphC { /*Explore servers searchbar glow*/
    border: 1px solid rgba(var(--server-channel-textc), 0.35);
    border-radius: var(--button-radius);
    transition: 0.25s ease;
}
.search-1iTphC:hover { /*Explore servers searchbar hovered glow*/
    border: 1px solid rgba(var(--server-channel-textc), 0.65);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.search-1iTphC:focus-within { /*Explore servers searchbar focused glow*/
    border: 1px solid rgba(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.search-1iTphC .searchBox-2_mAlO .searchBoxInput-K6mkng,
.search-1iTphC .searchBox-2_mAlO .colorMuted-HdFt4q {
    color: rgb(var(--server-channel-textc));
}
.search-1iTphC .searchBox-2_mAlO .closeIcon-2WLZc1 { /*Close button*/
    color: rgb(var(--server-channel-textc));
}
.card-3DjzTQ { /*Public servers card*/
    border-radius: var(--main-radius);
    background-color: rgba(var(--main-dark-color), 0.35)!important;
    transition: filter 0.25s ease;
}
.card-3DjzTQ:hover { /*Public servers card*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.iconMask-3b8GzQ { /*Public servers icon*/
    background-color: transparent!important;
}
.categoryItem-1QIroW { /*Explore categories*/
    color: rgb(var(--server-channel-textc));
    filter: opacity(0.2);
    transition: filter 0.25s ease;
}
.categoryItem-1QIroW:hover { /*Explore hovered*/
    background-color: transparent;
    color: rgb(var(--server-channel-textc));
    filter: opacity(0.55) drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.categoryItem-1QIroW.selectedCategoryItem-FHKU_o { /*Explore selected*/
    color: rgb(var(--server-channel-textc));
    background-color: transparent;
    filter: opacity(1) drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.categoryItem-1QIroW:hover .layout-2DM8Md,
.categoryItem-1QIroW.selectedCategoryItem-FHKU_o .itemInner-gPkiWb { /*Explore hovered/selected background*/
    background-color: transparent;
}

/*Create server*/

.root-1gCeng { /*Main modal*/
    background: transparent!important;
    border-radius: var(--main-radius);
}
.root-1gCeng::before { /*Main modal background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--popout-bg) center/cover no-repeat;
    border-radius: var(--main-radius);
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.root-1gCeng::after { /*Main modal opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.templatesList-2E6rTe .container-UC8Ug1,
.optionsList-3UMAjx .container-UC8Ug1 { /*Server templates*/
    background-color: transparent;
    border-color: transparent;
}
.header-3msK0M .title-3w8xhj,
.header-1BLHoL .title-LqAd9K,
.header-287ONi .title-Z_XiOC,
.header-1Xr5FO .title-XLSR78 { /*Create server header color*/
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.colorHeaderSecondary-3Sp3Ft { /*Subtitle*/
    color: rgba(var(--server-channel-textc), 0.85);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.footer-2gL1pp .footerTitle-2CYZch {
    color: rgb(var(--server-channel-textc), 0.55);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.templatesList-2E6rTe .container-UC8Ug1 .colorStandard-2KCXvj,
.optionsList-3UMAjx .container-UC8Ug1 .colorStandard-2KCXvj { /*Server templates text*/
    color: rgb(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.templatesList-2E6rTe .container-UC8Ug1:hover .colorStandard-2KCXvj,
.optionsList-3UMAjx .container-UC8Ug1:hover .colorStandard-2KCXvj { /*Server templates text*/
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.container-UC8Ug1 .icon-QM5383 { /*Template icon*/
    transition: 0.25s ease;
}
.container-UC8Ug1:hover .icon-QM5383 { /*Template icon hovered*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.backButton-iA7KIs,
.footer-2gL1pp .button-38aScr .contents-18-Yxp { /*Back button*/
    color: rgb(var(--server-channel-textc), 0.35);
    transition: color 0.25s ease;
}
.backButton-iA7KIs:hover,
.footer-2gL1pp .button-38aScr:hover .contents-18-Yxp  { /*Back button hovered*/
    color: rgb(var(--server-channel-textc), 0.85);
}
.footer-2gL1pp .button-38aScr:hover .contents-18-Yxp { /*Back button hovered*/
 background-image: none!important;
}
.content-1LAB8Z .input-cIJ7To { /*Server name input*/
    color: rgb(var(--server-channel-textc));
}
.iconContainer-2B0ixr svg circle { /*Upload picture circle*/
    fill: rgb(var(--server-channel-textc), 0.35)!important;
    transition: 0.25s ease;
}
.iconContainer-2B0ixr:hover svg circle  { /*Upload picture circle hovered*/
    fill: rgb(var(--server-channel-textc), 0.65)!important;
}
.input--jS-j2 { /*Join server with link*/
    background-color: transparent;
    border-radius: var(--button-radius);
}
.input--jS-j2 .inputDefault-_djjkz {
    color: rgba(var(--server-channel-textc), 0.2)!important;
}
.content-1LAB8Z .formTitle-aeXUoN {
    color: rgb(var(--server-channel-textc));
}
.examplesForm-1PzAn- .sampleLink-2NLvZg {
    color: rgba(var(--server-channel-textc), 0.6);
}
.closeButton-1tv5uR path { /*Close button style*/
    fill: rgb(var(--server-channel-textc), 0.35)!important;
}
.closeButton-9dkb_x svg,
.closeButton-9dkb_x path { /*Close button/ESC text animation*/
    transition: .25s ease;
}
.closeButton-9dkb_x:hover { /*Close button hover*/
    background-color: transparent!important;
}
.closeButton-9dkb_x:hover svg {
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.closeButton-9dkb_x :hover path { /*Close button hover*/
    fill: rgb(var(--server-channel-textc), 1)!important;
}

/*Server config*/

.divider-3wNib3,
.divider-Uf0Wob { /*divider*/
    display: none;
}
.container-_phMUq,
.container-_phMUq:hover,
.roleRow-30TwGe:hover:not(.roleRowDisableHover-1HiqqT) { /*Role options*/
    background-color: transparent;
}
.container-_phMUq,
.roleRow-30TwGe:not(.roleRowDisableHover-1HiqqT) .dragIcon-I74byJ,
.roleRow-30TwGe:not(.roleRowDisableHover-1HiqqT) .roleNameContainer-2o4-eI,
.roleRow-30TwGe:not(.roleRowDisableHover-1HiqqT) .memberCountContainer-1BJFU2,
.emojiRow-zIc7ZX .emojiImage-1hZi2F,
.emojiRow-zIc7ZX .emojiUploader-1f0pVx { /*Role options*/
    color: rgb(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.container-_phMUq:hover,
.roleRow-30TwGe:hover:not(.roleRowDisableHover-1HiqqT) .dragIcon-I74byJ,
.roleRow-30TwGe:hover:not(.roleRowDisableHover-1HiqqT) .roleNameContainer-2o4-eI,
.roleRow-30TwGe:hover:not(.roleRowDisableHover-1HiqqT) .memberCountContainer-1BJFU2,
.emojiRow-zIc7ZX:hover .emojiImage-1hZi2F,
.emojiRow-zIc7ZX:hover .emojiUploader-1f0pVx { /*role options hovered*/
    color: rgb(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.roleRow-30TwGe:hover:not(.roleRowDisableHover-1HiqqT) .circleButton-3RB01i,
.icon-3_8HGa { /*Role panel icons background*/
    background-color: transparent;
}
.roleRow-30TwGe:before,
.roleRow-30TwGe:last-child:after { /*Role dividers*/
    display: none;
}
.tableHeader-3x_1oD { /*Role titles*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.titleContainer-2CXtJo,
.header-2mZ9Ov { /*Roles back button*/
    background-color: transparent;
}
.header-2mZ9Ov { /*Text*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.titleElevated-c_kdi7 { /*shadow thingy*/
    box-shadow: unset;
}
.stickyHeaderElevated-I6QUOA {
    background-color: rgba(0, 0, 0, 0.55);
    backdrop-filter: blur(5px);
    border-bottom-left-radius: var(--main-radius);
    border-bottom-right-radius: var(--main-radius);
}
.sidebar-dLM-kh { /*Divider*/
    border: none;
}
.tabBar-11f3uI { /*Tab bar border*/
    border: none;
}
.emojiRow-zIc7ZX { /*Emoji hovered*/
    box-shadow: unset!important;
}
.emojiAliasInput-1y-NBz .emojiInput-1aLNse { /*Emoji name*/
    background-color: transparent!important;
}
.emojiRow-zIc7ZX .emojiRemove-1k6MlJ {
    background-color: transparent!important;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
    box-shadow: none!important;
    transition: filter 0.25s ease, opacity 0.25s ease;
}
.auditLog-3jNbM6 { /*Audit log main modal*/
    border: none;
    transition: 0.25s ease;
}
.auditLog-3jNbM6:hover { /*Audit log hovered*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.header-GwIGlr { /*Audit log subcontainer*/
    background-color: transparent!important;
}
.cardPrimaryEditable-3KtE4g { /*Integrations*/
    background-color: transparent;
    border: none;
}
.iconWrapper-lS1uig { /*Integration icons*/
    background-color: transparent;
}
.iconWrapper-lS1uig,
.secondaryHeader-2oeRPO,
.featureIcon-3huAlM,
.sectionHeader-roK2A- { /*Shadows*/
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.card-o7rAq- .horizontal-1ae9ci>.flex-1xMQg5 .colorStandard-2KCXvj,
.caret-Ld-w32 { /*Integration nage text and icon*/
    color: rgb(var(--server-channel-textc), 0.25);
    transition: 0.25s ease;
}
.card-o7rAq-:hover .horizontal-1ae9ci>.flex-1xMQg5 .colorStandard-2KCXvj,
.card-o7rAq-:hover .caret-Ld-w32 { /*Integration text and icon*/
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.descriptionBox-1EKQKL { /*Server template*/
    background-color: transparent;
}
.featureCard-1RR4Tl,
.featureIcon-3p1TC_ { /*Enable community feature card*/
    background-color: transparent;
}
.separator-3wQM3d { /*Divider*/
    display: none;
}
.member-1q7VfX { /*Server member*/
    box-shadow: unset!important;
}
.member-1q7VfX .avatar-2tTaT6, 
.member-1q7VfX .nameTag-3wmDUk { /*Server member elements*/
    transition: 0.25s ease;
}
.member-1q7VfX:hover .avatar-2tTaT6,
.member-1q7VfX:hover .nameTag-3wmDUk { /*Server member hovered elements*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
    box-shadow: unset!important;
}
.memberRow-1wwtfV:hover { /*Member hovered*/
    background-color: transparent;
}
.container-3XJ8ns { /*Role dropdown box*/
    border-radius: var(--main-radius);
    background-color: transparent;
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569), -3px -6px 10px 10px rgba(0, 0, 0, 0.569);
    border: none;
}
.container-3XJ8ns::before { /*Role dropdown box background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--popout-bg) center/cover no-repeat;
    border-radius: var(--main-radius);
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.container-3XJ8ns::after { /*Role dropdown box opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.container-3XJ8ns .item-2J2GlB { /*Dropdown roles*/
    filter: opacity(0.5);
    transition: 0.25s ease;
}
.container-3XJ8ns .item-2J2GlB:hover { /*Dropdown roles*/
    background-color: transparent;
    filter: opacity(1) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.customScroller-26gWhv > div .defaultColor-1_ajX0 { /*Header shadow*/
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.inviteSettingsInviteRow-3p2O-N { /*Server invite links*/
    box-shadow: unset!important;
    color: rgb(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.inviteSettingsInviteRow-3p2O-N:hover { /*Server invite link hovered*/
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.inviteSettingsInviteRow-3p2O-N .revokeInvite-28N8uj {
    background-color: transparent;
    transition: .25s ease;
}
.inviteSettingsInviteRow-3p2O-N:hover .revokeInvite-28N8uj { /*Delete invite button*/
    background-color: transparent;
    box-shadow: unset;
}
.customScroller-26gWhv>div .h5-18_1nd { /*Subtitles*/
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.cardWarning-2yPNAa { /*Delete server warning*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.cardWarning-2yPNAa .warning-3AwWn_ {
    color: rgb(var(--server-channel-textc));
}
.cardWarning-2yPNAa+.spacing-ApfUws .h5-18_1nd {
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}
.lookFilled-1Gx00P.colorRed-1TFJan .contents-18-Yxp {
    color: red;
}
.lookFilled-1Gx00P.colorRed-1TFJan:hover .contents-18-Yxp {
    color: red;
}
.settingCard-3w2mVL,
.scroller-305q3I,
.cardFolder-28dwxo,
.settingCard-3w2mVL.active-1ytUzX { /*Channel role*/
    background-color: transparent;
}
.group-1WdBVp { /*Permissions buttons*/
    border:none;
}
.item-1yAxl1 { /*Permissions*/
    background-color: transparent;
}
.container-2VW0UT { /*Save changes*/
    background-color: rgba(0, 0, 0, 0.3)!important;
    backdrop-filter: blur(5px);
}

/*Invited to server*/

.contentWrapper-3WC1ID { /*Main modal*/
    border-radius: var(--main-radius)!important;
    background-color: transparent!important;
    background: transparent!important;
}
.contentWrapper-3WC1ID::before { /*Main modal background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--popout-bg) center/cover no-repeat;
    border-radius: var(--main-radius);
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.contentWrapper-3WC1ID::after { /*Main modal opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.pill-1dHPfk { /*Server members*/
    background-color: transparent;
}
.marginBottom20-32qID7 .inviteLargeIcon-HrAH61,
.marginBottom20-32qID7 .colorHeaderSecondary-3Sp3Ft,
.marginBottom20-32qID7 .title-2_aCTw,
.marginBottom20-32qID7 .activityCount-2GgGMq { /*Modal text*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}

/*Gif/Emote/Stickers panels*/

.drawerSizingWrapper-17Mss4,
.emojiPicker-3PwZFl { /*Main modal*/
    background: transparent;
    border-radius: var(--main-radius);
    animation: menuShow 0.25s ease;
    transform-origin: bottom;
}
.drawerSizingWrapper-17Mss4::before,
.emojiPicker-3PwZFl::before { /*Main modal background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--popout-bg) center/cover no-repeat;
    border-radius: var(--main-radius);
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.drawerSizingWrapper-17Mss4::after,
.emojiPicker-3PwZFl::after { /*Main modal opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.contentWrapper-SvZHNd { /*Subcontainers*/
    background-color: transparent;
}
.header-1TOWci,
.header-8ilj5e { /*Panel headers*/
    box-shadow: unset!important;
}
.navItem-3Wp_oJ .navButton-2gQCx- { /*Tab buttons*/
    color: rgba(var(--server-channel-textc), 0.2);
    transition: 0.25s ease;
}
.navItem-3Wp_oJ .navButton-2gQCx-:hover { /*Tab buttons hover*/
    color: rgba(var(--server-channel-textc), 0.65);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.navItem-3Wp_oJ .navButtonActive-1MkytQ { /*Selected tab*/
    color: rgba(var(--server-channel-textc), 1)!important;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
    background-color: transparent;
}
.container-2XeR5Z,
.container-cMG81i { /*Searchbars bg*/
    background-color: transparent;
}
.searchBar-5di9mG,
.searchBar--fTZYa { /*Searchbar main*/
    border: 1px solid rgb(var(--server-channel-textc), 0.25);
    border-radius: var(--button-radius);
    transition: 0.25s ease;
}
.searchBar-5di9mG:hover,
.searchBar--fTZYa:hover { /*Searchbar hovered*/
    border: 1px solid rgb(var(--server-channel-textc), 0.45);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.searchBar-5di9mG:focus-within,
.searchBar--fTZYa:focus-within { /*Searchbar focused*/
    border: 1px solid rgb(var(--server-channel-textc), 1);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.categoryFadeBlurple-1j72_A { /*Gif foreground*/
    background-color: transparent!important;
    transition: bacground-color 0.25s ease;
}
.categoryFadeBlurple-1j72_A:hover { /*Gif foreground*/
    background-color: rgb(0, 0, 0, .35)!important;
}
.result-3w1ZcL:hover { /*Hovered result*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
    transition: 0.25s ease;
}
.result-3w1ZcL:hover::after { /*Hovered result ring*/
    box-shadow: none!important;
}
.categoryIcon-1SvUHG { /*Emoji category icon*/
    color: rgb(var(--server-channel-textc))!important;
}
.categoryItemDefaultCategory-aBZ6nJ { /*Emoji category*/
    filter: opacity(0.2);
    transition: 0.25s ease;
}
.categoryItemDefaultCategory-aBZ6nJ:hover { /*Emoji category hovered*/
    background-color: transparent;
    filter: opacity(0.65) drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.categoryItemDefaultCategorySelected-_HCKoz,
.categoryItemDefaultCategorySelected-_HCKoz:hover { /*Selected emoji category*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.guildIcon-3h-1IH { /*Guild category*/
    background-color: transparent;
}
.categoryItemGuildCategory-3MisqI foreignObject { /*Guild category avatar*/
    mask: none!important;
    border-radius: 50%;
}
.header-19cWci { /*Emote category expandable*/
    color: rgba(var(--server-channel-textc), 0.2);
    transition: 0.25s ease;
}
.header-19cWci:hover { /*Emote category expandable*/
    color: rgba(var(--server-channel-textc), 0.65)!important;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.header-19cWci[aria-expanded="true"] { /*Emote category expanded*/
    color: rgba(var(--server-channel-textc), 1)!important;
    backdrop-filter: blur(5px);
    border-radius: var(--button-radius);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.emojiItem-14v6tW.emojiItemSelected-1aLkfV { /*Hovered emoji*/
    transition: filter 0.25s ease;
}
.inspector-S2gM3e,
.emojiItem-14v6tW.emojiItemSelected-1aLkfV  { /*Hovered emoji*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.guildCategorySeparator-_An-MP { /*Category divider*/
    display: none;
}
.emojiPickerInExpressionPicker-3IzIcv .emojiPicker-3PwZFl { /*Box shadow overflow*/
    overflow: visible!important;
}
.diversitySelector-1v4_1A { /*Selected diversity*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.diversitySelectorOptions-4YM-vX { /*Diversity selector*/
    background-color: transparent;
    border: none;
    box-shadow: -3px -3px 5px 1px black;
}
.diversitySelectorOptions-4YM-vX::before { /*Diversity selector background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--popout-bg) center/cover no-repeat;
    border-radius: var(--main-radius);
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.diversitySelectorOptions-4YM-vX::after { /*Diversity selector opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.diversityEmojiItem-L6_IXw { /*Diversity button*/
    transition: 0.25s ease;
}
.diversityEmojiItem-L6_IXw:hover { /*Diversity selector hovered*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.emojiSection-3Fb9ix { /*Clicked emoji in chat*/
    background-color: transparent;
    background: transparent;
    border-radius: var(--main-radius);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.emojiSection-3Fb9ix::before { /*Clicked emoji in chat*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--popout-bg) center/cover no-repeat;
    border-radius: var(--main-radius);
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.emojiSection-3Fb9ix::after { /*Clicked emoji in chat*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.popoutContainer-1MXdqN { /*Popout modal*/
    background: transparent;
    border-radius: var(--main-radius);
    box-shadow: unset;
}
.header-2k4I2o { /*Stickers panel*/
    box-shadow: unset;
}
.stickerInspected-2EM4w- .inspectedIndicator-59EII8 { /*Hovered sticker*/
    background-color: transparent;
}

/*Server boost*/

.perksModal-fSYqOq { /*Main modal*/
    top: 50%!important;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
    width: var(--settings-width);
    height: calc(var(--settings-heigth) - 5%);
    background: var(--popout-bg) center/cover !important;
    border-radius: var(--main-radius);
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569), -3px -6px 10px 10px rgba(0, 0, 0, 0.569);
    pointer-events: all!important;
}
.root-3R2ngo .closeButton-1tv5uR::before { /*Close button left backdrop*/
    content: '';
    position: fixed;
    top: 0;
    left: 0;
    width: calc(80% - var(--settings-width));
    height: 100%;
    cursor: pointer;
    pointer-events: inherit;
    transition: 0.25s ease-in;
}
.root-3R2ngo .closeButton-1tv5uR::after { /*Close button right backdrop*/
    content: '';
    position: fixed;
    top: 0;
    left: calc(20% + var(--settings-width));
    width: calc(80% - var(--settings-width));
    height: 100%;
    cursor: pointer;
    pointer-events: inherit;
    transition: 0.25s ease-in;
}
.root-3R2ngo .closeButton-1tv5uR:active { /*Makes the window dissapear*/
    transform: none;
}
.ctaBar-2UsjF2 { /*Server container*/
    background-color: transparent;
    background-image: url()!important;
}
.container-1sFeqf { /*Close window button*/
    right: -35%;
    top: 80px;
}
.carousel-18mXWH { /*Server level panels*/
    left: 15px!important;
}
.tierWrapper-W9ajqp { /*Server tier wrappers*/
    border-radius: var(--button-radius);
    background-color: transparent;
    box-shadow: unset!important;
}
.tierMarkerBackground-3q29am { /*Server boost level progress bar*/
    background-color: transparent!important;
}
.iconWrapper-3LVgIo { /*Server boost quantity*/
    background: transparent!important;
}
.iconWrapper-3LVgIo:hover { /*Server boost quantity hover*/
    background: rgb(var(--accent-color), 0.55)!important;
}
.icon-TYbVk4, .icon-TYbVk4.disabled-24YXy-,
.icon-TYbVk4.disabled-24YXy-:hover { /*Server boost quantity*/
    color: rgb(var(--server-channel-textc));
}
.tier-12tKuZ { /*Server boost tier container*/
    border-radius: var(--button-radius);
}
.tierBody-16Chc9 { /*Server boost tier card body*/
    background-color: transparent!important;
}
.perk-2WeBWW { /*Server boost perks*/
    background-color: transparent!important;
}
.divider-25_-sM { /*Server boost divider*/
    background-color: transparent;
}
.tier-3H4BXk { /*Server boost tier main modal*/
    border-radius: var(--main-radius);
}
.tierBody-x9kBBp { /*Server boost tier body*/
    background-color: rgba(0, 0, 0, 0.15)!important;
}
.tierHeaderLocked-1a2opw { /*Server boost tier header*/
    background-color: rgba(0, 0, 0, 0.35)!important;
}
.upsellFooter-3coAfO,
.value-IR9osW  { /*Buying boosts*/
    background-color: transparent;
}
.content-2qfHzC .headerGraphic-nVhv-X,
.content-2qfHzC .headerBlurb-1GxBrq,
.content-2qfHzC .ctaBar-2UsjF2,
.subscriberPerksHeader-2a50UC,
.perks-3OsGy8,
.wrapper-1hrFc0,
.wrapper-3nSjSv .heading-4znNKq,
.wrapper-3nSjSv:before { /*Server boost title*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.carouselItemSelected-JFUsnG { /*Achieved boost tier*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.tierHeaderLocked-1s2JJz { /*Locked tier*/
    color: rgb(var(--server-channel-textc))!important;
    background-color: transparent!important;
    filter: opacity(0.5);
}
.planSelectDivider-3KU5-l { /*Buy boost divider*/
    display: none;
}
.breadcrumbsWrapper-1m9gjf { /*Buy boost divider*/
    border-bottom: none;
}
.tierBody-3aUxuc,
.tierHeaderLocked-3S508x {
    background-color: transparent!important;
}
.tierHeaderLocked-3S508x {
    border-bottom: 1px solid rgb(var(--server-channel-textc));
}

/*Channel preview/Stream preview*/

.streamPreview-2-WUWT,
.container-2dqNWc { /*Stream preview*/
    background-color: transparent!important;
    background: transparent!important;
    border-radius: var(--main-radius);
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569);
}
.streamPreviewWrapper-2DSWOK.mounted-26niXS::before { /*Stream preview background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;    
    right: 0;
    bottom: 0;
    background: var(--popout-bg) center/cover no-repeat;
    border-radius: var(--main-radius);
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.streamPreviewWrapper-2DSWOK.mounted-26niXS::after { /*Stream preview opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.container-2dqNWc {
    overflow: auto!important;
}
.container-2dqNWc::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--popout-bg) center/cover no-repeat;
    border-radius: var(--main-radius);
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.container-2dqNWc::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.watchButton-2SbJEo,
.button-uXr0L2 { /*Join stream button*/
    border-radius: var(--button-radius);
    color: rgba(var(--server-channel-textc), 0.35);
    border-color: rgba(var(--server-channel-textc), 0.35)!important;
    transition: 0.25s ease;
}
.watchButton-2SbJEo.button-38aScr:disabled,
.button-uXr0L2:disabled { /*Disabled join stream button*/
    color: rgba(var(--server-channel-textc), 0.15);
    border-color: rgba(var(--server-channel-textc), 0.15)!important;
}
.watchButton-2SbJEo:hover:not(:disabled),
.button-uXr0L2:hover:not(:disabled) { /*Join stream button hovered*/
    color: rgba(var(--server-channel-textc), 1)!important;
    border-color: rgba(var(--server-channel-textc), 1)!important;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.previewContainer-12UlHl { /*Stream preview container*/
    background-color: transparent!important;
}
.activity-3jdl2U+.activity-3jdl2U { /*Divider*/
    border-top: none;
}
.activity-3jdl2U { /*Channel preview activity*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}

/*Watch party thingy*/

.scroller-1SuHJo,
.callContainer-3UuV6S,
.container-pTf0Ly,
.rowContainer-2tYerQ,
.container-2t1JyW,
.participants-soO0aD { /*Main modals*/
    background-color: transparent;
}
.divider-JMvf_l {
    border: none;
}
.container-2t1JyW,
.rowContainer-2tYerQ,
.roleContainer-8-Ld9g { /*Shadows*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.tileContainer-BaRAZF { /*Users*/
    transition: 0.25s ease;
}
.tileContainer-BaRAZF:hover { /*User hovered*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.auto-3V-QBl::-webkit-scrollbar-thumb { /*Scrollbar thumb*/
    background-color: rgb(var(--main-dark-color))!important;
}
.auto-3V-QBl::-webkit-scrollbar-thumb,
.auto-3V-QBl::-webkit-scrollbar-track { /*Scrollbar thing*/
    border: none;
}
.participantsButton-KYW-IW,
.cta-3gK0Pu { /*Call participants button*/
    background-color: rgba(0,0,0,.3);
}
.participantsButton-KYW-IW:hover,
.cta-3gK0Pu:hover { /*Call participants button hovered*/
    background-color: rgba(0,0,0,.6);
}
.separator-2-RRj_ { /*Invite separator*/
    box-shadow: unset!important;
}
.inviteRow-2L02ae { /*Invite friend to channel*/
    color: rgb(var(--server-channel-textc), 0.35);
    transition: 0.25s ease;
}
.inviteRow-2L02ae:hover { /*Invite friend to channel hovered*/
    background-color: transparent!important;
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
}

/*Stage Discovery*/

.stageSection-3mAD8V { /*Main modal*/
    background-color: transparent;
}
.headerBarContainer-31FKNA { /*Header shadow underline*/
    box-shadow: none;
}
.container-S9SaVf { /*Stage cards*/
    border-radius: 8px;
    background: var(--popout-bg) center/cover no-repeat;
    box-shadow: 0px 0px 0px 0px rgba(0, 0, 0, 0.569);
    border: unset;
    transition: box-shadow .25s ease;
}
.container-S9SaVf:hover { /*Active now cards*/
    box-shadow: -3px -3px 5px 3px rgba(0, 0, 0, 0.569);
}
.container-S9SaVf .topicText-3B26Cx { /*Stage card title*/
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.container-7Unqij,
.iconMicrophone-1A2Yqh,
.speakerCount-3KijLY { /*Card icons*/
    background-color: transparent;
}
.container-2rNpDV { /*Stage picture*/
    background-color: transparent;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.pageHeader-3nuK1W { /*Live stages title text*/
    color: rgb(var(--server-channel-textc));
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
    text-align: center;
}
.bulletsContainer-3omDLR,
.circle-1anBj0 { /*Create stage*/
    background-color: transparent;
}
.bulletsContainer-3omDLR,
.header-1AQlNL { /*Create stage text*/
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
}
.header-1AQlNL {
    color: rgb(var(--server-channel-textc));
}
.borderBottom-cijHjW { /*Divider*/
    border: none;
}

/*Threads*/

.container-7uh5fX { /*Main modal*/
    background: transparent;
    border-radius: var(--main-radius);
    animation: menuShow 0.25s ease;
    transform-origin: bottom;
}
.container-7uh5fX::before { /*Main modal background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--popout-bg) center/cover no-repeat;
    border-radius: var(--main-radius);
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.container-7uh5fX::after { /*Main modal opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: var(--main-radius);
    background-color: rgba(0,0,0, var(--popout-opacity));
    z-index: -1;
}
.header-1VS4tm {
    background-color: transparent;
}
.header-1VS4tm .tabBar-31Wimb .tab-PQvTH4,
.list-wek7hJ .tabBar-wS4pjJ .tab-17bjMB { /*Tab buttons*/
    color: rgba(var(--server-channel-textc), 0.2);
    transition: 0.25s ease;
}
.header-1VS4tm .tabBar-31Wimb .tab-PQvTH4:hover,
.list-wek7hJ .tabBar-wS4pjJ .tab-17bjMB:hover { /*Tab buttons hover*/
    color: rgba(var(--server-channel-textc), 0.65);
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
    background-color: transparent!important;
}
.header-1VS4tm .tabBar-31Wimb .tab-PQvTH4.active-30vPlA,
.list-wek7hJ .tabBar-wS4pjJ .tab-17bjMB.active-3JUHqX { /*Selected tab*/
    color: rgba(var(--server-channel-textc), 1)!important;
    filter: drop-shadow(-3px -1px 1px black) drop-shadow(-2px 0px 1px black);
    background-color: transparent!important;
}
.divider-mDc_D8 { /*Divider*/
    background: transparent;
}
.icon-3pEw1v { /*svg background*/
    background: transparent;
}
.row-1ImlrZ {
    color: rgb(var(--server-channel-textc))!important;
    filter: opacity(0.2);
    transition: filter .25s ease;
}
.row-1ImlrZ:hover {
    filter: opacity(0.45) drop-shadow(-3px -1px 1px rgb(0, 0, 0)) drop-shadow(-3px -1px 1px rgb(0, 0, 0));
    background: none;
}
.chatHeaderBar-4vZS1x {
    height: 20px;
    border-bottom-left-radius: 20px;
    border-bottom-right-radius: 20px;
    background: var(--popout-bg);
    background-color: transparent;
    box-shadow: -3px -4px 6px 3px black;
    opacity: 1;
}

/*Misc*/

.ring-13rgEW { /*Ring when tabbing*/
    box-shadow: none;
}
.keyboard-mode .focusStroke-1ApElc { /*Focused element with keyboard*/
    fill: none;
    stroke: none;
}
.mediaBarGrabber-1FqnbN,
.mediaBarProgress-1xaPtl,
.mediaBarProgress-1xaPtl:after,
.mediaBarProgress-1xaPtl:before { /*Stream volume bar*/
    background-color: rgba(var(--accent-color), 0.85)!important;
}
.small-1CUeBa { /*Uploading colored bar*/
    background-color: var(--accent-color)!important;
}
.progress-3Rbvu0 { /*Uploading remaining bar*/
    background-color: rgb(0, 0, 0, 0.65)!important;
}
.mediaBarWrapper-3D7r67,
.mediaBarWrapper-3D7r67:after,
.mediaBarWrapper-3D7r67:before { /*Audio progress bar*/
    background-color: rgb(0, 0, 0, 0.65);
}
.buffer-26XPkd,
.buffer-26XPkd:after,
.buffer-26XPkd:before { /*Audio buffer bar*/
    background-color: rgba(var(--accent-color), 0.5);
}
.mediaBarPreview-1jfyFs,
.mediaBarPreview-1jfyFs:after,
.mediaBarPreview-1jfyFs:before { /*Audio hover*/
    background-color: rgba(var(--accent-color), 0.7);
}
@keyframes tooltipShow {
    0% {
        transform: scale(0);
    }
    100% {
        transform: scale(1);
    }
}
.tooltip-2QfLtc,
.toolbar-2bjZV7,
.scroller-2ymjU1,
.popout-APcvZm { /*Hovered element tooltip*/
    filter: drop-shadow(-3px -2px 1px black) drop-shadow(-3px -1px 1px black);
    background-color: transparent!important;
    background: transparent!important;
    border-radius: var(--main-radius);
    animation: tooltipShow 0.15s ease-in;
    color: rgb(var(--server-channel-textc))!important;
    box-shadow: unset!important;
}
.tooltip-2QfLtc::before,
.scroller-2ymjU1::before,
.popout-APcvZm::before { /*Stream preview background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--popout-bg) center/cover no-repeat;
    border-radius: var(--main-radius);
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.tooltip-2QfLtc::after,
.scroller-2ymjU1::after, 
.popout-APcvZm::after { /*Stream preview opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(0,0,0, var(--popout-opacity));
    border-radius: var(--main-radius);
    z-index: -1;
}
.memberListItem-3IkoL8:not(.popoutDisabled-161HX0):hover { /*Hovered stream viewer*/
    background-color: transparent!important;
    filter: drop-shadow(-3px -2px 1px black) drop-shadow(-3px -1px 1px black);
}
.tooltip-2QfLtc .reactionTooltipContent-2TwEIL {
    filter: drop-shadow(-3px -2px 1px black) drop-shadow(-3px -1px 1px black);
}
.tooltipPointer-3ZfirK { /*Hovered element tooltip arrow*/
    border-top-color: rgb(var(--main-dark-color))!important;
}
.protip-1b9XPC {
    border-top: none;
}
.applicationName-1-Uq7y.clickable-1bVtEA:hover,
.commandName-1klrjB.clickable-1bVtEA:hover,
.username-1A8OIy.clickable-1bVtEA:hover { /*Various underlines when hovering*/
    text-decoration: none;
}
.moreUsers-7v8yWY { /*more users in channel tooltip*/
    background-color: transparent;
}
.content-1T5kuS { /*Can't detect camera modal*/
    filter: drop-shadow(-3px -2px 1px black) drop-shadow(-3px -1px 1px black);
}
.keyboardShortcutsModal-3piNz7 { /*KB Shortcuts*/
    background-color: transparent!important;
    background: transparent!important;
    border-radius: var(--main-radius);
    box-shadow: -3px -6px 10px 10px rgba(0, 0, 0, 0.569);
}
.keyboardShortcutsModal-3piNz7::before { /*KB Shortcuts background*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--popout-bg) center/cover no-repeat;
    border-radius: var(--main-radius);
    filter: blur(var(--popout-blur));
    z-index: -2;
}
.keyboardShortcutsModal-3piNz7::after{ /*KB Shortcuts opacity*/
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(0,0,0, var(--popout-opacity));
    border-radius: var(--main-radius);
    z-index: -1;
}
.modalSubtitle-1Pj5nv { /*KB modal subtitle*/
    border-bottom: none!important;
}
.modalTitle-37O4n6,
.modalSubtitle-1Pj5nv { /*Keyboard modal text*/
    filter: drop-shadow(-3px -2px 1px black) drop-shadow(-3px -1px 1px black);
    color: rgb(var(--server-channel-textc))!important;
}
::selection,
.highlight { /*Selection and matched words*/
    background-color: rgba(var(--accent-color), 0.25);
}
.stageListenerPill-1RXT2G { /*Tooltip listening icon*/
    background-color: transparent;
}
.featuredTag-3pT1Rf { /*Featured tag*/
    background-color: transparent!important;
}
.featuredTagText-HmlSoA { /*Featured tag text*/
    color: rgb(var(--accent-color));
}
.active-2HPddW,
.hover-28QbSq:hover { /*Selected text toolbar option*/
    background-color: transparent;
}
.toolbar-2bjZV7:before { /*Selected text toolbar tip*/
    border-top-color: rgb(var(--accent-color));
}
.compactButton-195WSV, 
.compactButtonDisabled-1WXLm6 { /*New DM message*/
    background-color: transparent!important;
}
.badge-1JXQev { /*Streaming icon*/
    background-color: transparent;
}
.textBadge-1iylP6 { /*Banner nitro badge*/
    background-color: transparent!important;
}
.sidebarContainer-7fi3LO { /*Hubs sidebar*/
    background: transparent;
}
.modal-f02hVt,
.guildSidebar-2OCzWB,
.formFieldWrapper-malor5 { /*Rules modal*/
    background: transparent;
}

/*Plugins compatibility*/

/*Member Count*/
#MemberCount { /*Styling*/
    margin-left: 8px!important;
    background: transparent!important;
}
