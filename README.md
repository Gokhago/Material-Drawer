# Material-Drawer
Material Drawer
header for drawer
```html
<div class="header" id="headerq">
    <div class="rx_icon" id="rx_icon"></div>
    <div class="titleq" id="title">Title Drawer</div>
</div>
```
add a drawer
```html
<div class="container">
    <div class="content">
      html content here
  </div>
</div>
    </div>
</div>
<div class="drawer" id="drawer">
    <div class="content">
        <div class="header">
            <div class="avatar"></div>
            <div class="text">
                <div class="field name"></div>
                <div class="field info"></div>
            </div>
        </div>
        html content here
    </div>
</div>
```
add a javascript code
```javascript
var drawer,
    drawerElem,
    iconElem;

    drawerElem = document.getElementById("drawer");
    iconElem = document.getElementById("rx_icon");
    drawer = new Drawer(drawerElem);
    drawer.setDrawerIcon(new DrawerIcon(iconElem));
    
    //Use methods
    drawer.onOpenListener(function () {
        console.log("open");
    });
    drawer.onCloseListener(function () {
        console.log("close");
    });
    drawer.onMoveListener(function (x, percent, animation, duration) {
        console.log(x + " " + percent + " " + animation + " " + duration);
    });
    drawer.openDrawer();
    drawer.closeDrawer();
    drawer.toggleDrawer();
    drawer.isOpen();
    drawer.resetIconOnClick();
```
# Library
add a css library
```css
 #headerq {
	 height: 56px;
	 background: #687894;
	 position: fixed;
	 top: 0;
	 left: 0;
	 right: 0;
	 width: 100%;
	 z-index: 3;
	 box-shadow: 0 3px 6px -3px rgba(0,0,0,0.5);
}
 #headerq .rx_icon {
	 float: right;
	 height: 56px;
	 width: 56px;
}
 #headerq .titleq {
	 height: 100%;
	 line-height: 56px;
	 padding-left: 16px;
	 padding-right: 8px;
	 float: right;
	 color: white;
	 font-size: 18px;
}
 .drawer .content {
	 height: 100%;
	 position: relative;
	 overflow-y: auto;
}
 .drawer .content .header {
	 height: 144px;
	 background: #687894;
	 position: relative;
}
 .drawer .content .header .avatar {
	 background-image: url('https://s3-us-west-2.amazonaws.com/s.cdpn.io/225694/profile/profile-512_1.jpg');
	 height: 64px;
	 width: 64px;
	 background-position: center;
	 background-repeat: no-repeat;
	 background-size: cover;
	 border-radius: 100%;
	 position: absolute;
	 left: 16px;
	 top: 16px;
}
 .drawer .content .header .text {
	 height: 56px;
	 position: absolute;
	 bottom: 0;
	 left: 0;
	 width: 100%;
	 box-sizing: border-box;
	 padding: 8px 0;
	 color: white;
}
 .drawer .content .header .text .field {
	 padding-left: 16px;
	 font-size: 14px;
}
 .drawer .content .header .text .field.name {
	 font-weight: bold;
}
 .drawer .content .header .text .field.info {
	 margin-top: 4px;
}
 .drawer .content ul.menu {
	 padding: 8px 0;
	 list-style: none;
	 margin: 0;
}
 .drawer .content ul.menu li.item {
	 display: block;
	 font-size: 14px;
	 font-weight: bold;
	 height: 48px;
	 line-height: 48px;
	 padding-left: 72px;
	 color: rgba(0,0,0,0.87);
	 position: relative;
}
 .drawer .content ul.menu li.item.subheader {
	 color: rgba(0,0,0,0.54);
	 padding-left: 16px;
	 margin-top: 8px;
	 border-top: 1px solid rgba(0,0,0,0.12);
}
 .drawer .content ul.menu li.item.subheader:after {
	 content: none;
}
 .drawer .content ul.menu li.item:after {
	 content: "";
	 background-image: url('https://storage.googleapis.com/material-icons/external-assets/v4/icons/svg/ic_brightness_high_black_24px.svg');
	 background-position: center;
	 background-repeat: no-repeat;
	 background-size: cover;
	 height: 24px;
	 width: 24px;
	 position: absolute;
	 left: 16px;
	 top: 12px;
	 opacity: 0.54;
}
 .drawer .content ul.menu li.item:active {
	 background: rgba(0,0,0,0.12);
}
 .rx_noselect {
	 -webkit-touch-callout: none;
	 -webkit-user-select: none;
	 -khtml-user-select: none;
	 -moz-user-select: none;
	 -ms-user-select: none;
	 user-select: none;
}
 .drawer_bg {
	 position: fixed;
	 background: rgba(0,0,0,0.5);
	 top: 0;
	 left: 0;
	 right: 0;
	 bottom: 0;
	 width: 100%;
	 height: 100%;
	 z-index: 4;
	 opacity: 0.001;
	 -webkit-transform: translateZ(0);
	 -moz-transform: translateZ(0);
	 -ms-transform: translateZ(0);
	 -o-transform: translateZ(0);
	 transform: translateZ(0);
	 visibility: hidden;
}
 .drawer {
	 max-width: 320px;
	 width: 75%;
	 height: 100%;
	 left: 0px;
	 top: 0;
	 bottom: 0;
	 -webkit-transform: translateX(-100%);
	 -moz-transform: translateX(-100%);
	 -ms-transform: translateX(-100%);
	 -o-transform: translateX(-100%);
	 transform: translateX(-100%);
	 background: white;
	 position: fixed;
	 z-index: 5;
	 opacity: 0.001;
	 -webkit-box-shadow: 3px 0 16px -3px rgba(0,0,0,0.4);
	 -moz-box-shadow: 3px 0 16px -3px rgba(0,0,0,0.4);
	 -ms-box-shadow: 3px 0 16px -3px rgba(0,0,0,0.4);
	 -o-box-shadow: 3px 0 16px -3px rgba(0,0,0,0.4);
	 box-shadow: 3px 0 16px -3px rgba(0,0,0,0.4);
}
 .drawer .label {
	 position: absolute;
	 top: 56px;
	 bottom: 0;
	 width: 32px;
	 right: -32px;
}
 .drawer .antiSelect {
	 position: absolute;
	 top: 0;
	 left: 0;
	 height: 100%;
	 width: 100%;
	 visibility: hidden;
}
 .rx_icon {
	 position: relative;
	 height: 64px;
	 width: 64px;
}
 .rx_icon .ic {
	 position: absolute;
	 width: 24px;
	 height: 24px;
	 left: 50%;
	 margin-left: -12px;
	 top: 50%;
	 margin-top: -12px;
}
 .rx_icon .ic .line {
	 position: absolute;
	 left: 3px;
	 right: 3px;
	 height: 2px;
	 background: white;
	 outline: 1px solid transparent;
}
 .rx_icon .ic .line.one {
	 top: 6px;
	 -webkit-transform-origin: right bottom;
	 -moz-transform-origin: right bottom;
	 -ms-transform-origin: right bottom;
	 -o-transform-origin: right bottom;
	 transform-origin: right bottom;
}
 .rx_icon .ic .line.two {
	 top: 11px;
}
 .rx_icon .ic .line.thr {
	 transform-origin: right top;
	 -webkit-transform-origin: right top;
	 -moz-transform-origin: right top;
	 -ms-transform-origin: right top;
	 -o-transform-origin: right top;
	 top: 16px;
}
```
add a javascript library
```javascript
/* Drawer Library */
function Drawer(drawerElem) {
    "use strict";

    function checkMobile(a) {
        return /(android|bb\d+|meego).+mobile|avantgo|bada\/|blackberry|blazer|compal|elaine|fennec|hiptop|iemobile|ip(hone|od)|iris|kindle|lge |maemo|midp|mmp|mobile.+firefox|netfront|opera m(ob|in)i|palm( os)?|phone|p(ixi|re)\/|plucker|pocket|psp|series(4|6)0|symbian|treo|up\.(browser|link)|vodafone|wap|windows ce|xda|xiino|android|ipad|playbook|silk/i.test(a) || /1207|6310|6590|3gso|4thp|50[1-6]i|770s|802s|a wa|abac|ac(er|oo|s\-)|ai(ko|rn)|al(av|ca|co)|amoi|an(ex|ny|yw)|aptu|ar(ch|go)|as(te|us)|attw|au(di|\-m|r |s )|avan|be(ck|ll|nq)|bi(lb|rd)|bl(ac|az)|br(e|v)w|bumb|bw\-(n|u)|c55\/|capi|ccwa|cdm\-|cell|chtm|cldc|cmd\-|co(mp|nd)|craw|da(it|ll|ng)|dbte|dc\-s|devi|dica|dmob|do(c|p)o|ds(12|\-d)|el(49|ai)|em(l2|ul)|er(ic|k0)|esl8|ez([4-7]0|os|wa|ze)|fetc|fly(\-|_)|g1 u|g560|gene|gf\-5|g\-mo|go(\.w|od)|gr(ad|un)|haie|hcit|hd\-(m|p|t)|hei\-|hi(pt|ta)|hp( i|ip)|hs\-c|ht(c(\-| |_|a|g|p|s|t)|tp)|hu(aw|tc)|i\-(20|go|ma)|i230|iac( |\-|\/)|ibro|idea|ig01|ikom|im1k|inno|ipaq|iris|ja(t|v)a|jbro|jemu|jigs|kddi|keji|kgt( |\/)|klon|kpt |kwc\-|kyo(c|k)|le(no|xi)|lg( g|\/(k|l|u)|50|54|\-[a-w])|libw|lynx|m1\-w|m3ga|m50\/|ma(te|ui|xo)|mc(01|21|ca)|m\-cr|me(rc|ri)|mi(o8|oa|ts)|mmef|mo(01|02|bi|de|do|t(\-| |o|v)|zz)|mt(50|p1|v )|mwbp|mywa|n10[0-2]|n20[2-3]|n30(0|2)|n50(0|2|5)|n7(0(0|1)|10)|ne((c|m)\-|on|tf|wf|wg|wt)|nok(6|i)|nzph|o2im|op(ti|wv)|oran|owg1|p800|pan(a|d|t)|pdxg|pg(13|\-([1-8]|c))|phil|pire|pl(ay|uc)|pn\-2|po(ck|rt|se)|prox|psio|pt\-g|qa\-a|qc(07|12|21|32|60|\-[2-7]|i\-)|qtek|r380|r600|raks|rim9|ro(ve|zo)|s55\/|sa(ge|ma|mm|ms|ny|va)|sc(01|h\-|oo|p\-)|sdk\/|se(c(\-|0|1)|47|mc|nd|ri)|sgh\-|shar|sie(\-|m)|sk\-0|sl(45|id)|sm(al|ar|b3|it|t5)|so(ft|ny)|sp(01|h\-|v\-|v )|sy(01|mb)|t2(18|50)|t6(00|10|18)|ta(gt|lk)|tcl\-|tdg\-|tel(i|m)|tim\-|t\-mo|to(pl|sh)|ts(70|m\-|m3|m5)|tx\-9|up(\.b|g1|si)|utst|v400|v750|veri|vi(rg|te)|vk(40|5[0-3]|\-v)|vm40|voda|vulc|vx(52|53|60|61|70|80|81|83|85|98)|w3c(\-| )|webc|whit|wi(g |nc|nw)|wmlb|wonu|x700|yas\-|your|zeto|zte\-/i.test(a.substr(0, 4));
    }
    var drawerIcon = {
            set: function (a) {},
            setState: function (a, b) {},
            setOnClick: function(a) {}
        },
        drawerBg,
        drawerStarted = false,
        width = drawerElem.offsetWidth,
        correct = 0,
        percent = 0,
        trx = 0,
        opened = false,
        startMoveTime = 0,
        startX = 0,
        speedSwipe = 0,
        isMobile = checkMobile(navigator.userAgent || navigator.vendor || window.opera),
        isIE = window.navigator.msPointerEnabled,
        isIE11 = window.navigator.pointerEnabled,
        typeStart = isIE ? "MSPointerDown" : (isMobile ? "touchstart" : "mousedown"),
        typeMove = isIE ? "MSPointerMove" : (isMobile ? "touchmove" : "mousemove"),
        typeEnd = isIE ? "MSPointerUp" : (isMobile ? "touchend" : "mouseup"),
        trZ = "translateZ(0)",
        stateMoved = false,
        transformProp = "transform",
        transitionProp = "transition",
        propPrefixCss = "",
        antiSelect,
        onOpened = function () {},
        onClosed = function () {},
        onMove = function (x, percent, animation, duration) {};

    function setProperty(elem, property, value) {
        elem.style[property] = value;
    }

    function transfrom(x) {
        setProperty(drawerElem, transformProp, x + " " + trZ);
    }

    function move(x, e) {
        if (x < 0) {
            x = 0;
        }
        if (x > width) {
            x = width;
        }
        if (!stateMoved) {
            if (!isMobile) {
                antiSelect.style.visibility = "visible";
                if (!document.body.classList.contains("rx_noselect"))
                    document.body.classList.add("rx_noselect");
            }
            if (trx == x) {
                stateMoved = false;
                return;
            } else {
                e.preventDefault();
                stateMoved = true;
            }

        }
        trx = x;
        transfrom("translateX(-" + x + "px)");
        percent = (1 - (x / width));
        if (percent >= 1) {
            percent = 1;
        } else if (percent <= 0) {
            percent = 0;
        }
        drawerIcon.set(percent * 100);
        drawerBg.style.opacity = percent;
        onMove(320 - x, percent, false, 0);
    }

    function setTransition(s) {
        setProperty(drawerElem, transitionProp, propPrefixCss + "transform " + s + "s cubic-bezier(0.0, 0.0, 0.2, 1)");
        setProperty(drawerBg, transitionProp, "opacity " + s + "s cubic-bezier(0.0, 0.0, 0.2, 1)");
    }

    function clearTransition() {
        setProperty(drawerElem, transitionProp, "none");
        setProperty(drawerBg, transitionProp, "none");
    }

    function openDrawer(s) {
        s = s || 0.225;
        opened = true;
        setTransition(s);
        drawerElem.style.opacity = 1;
        drawerBg.style.opacity = 1;
        drawerBg.style.visibility = "visible";
        transfrom("translateX(0)");
        drawerIcon.setState(1, s);
        onMove(width, 1, true, s);
        setTimeout(function () {
            clearTransition();
            if (drawerStarted) {
                return;
            }
            onOpened();
        }, s * 1000);
    }

    function closeDrawer(s) {
        s = s || 0.225;
        opened = false;
        setTransition(s);
        drawerBg.style.opacity = 0.001;
        transfrom("translateX(-" + width + "px)");
        drawerIcon.setState(0, s);
        onMove(0, 0, true, s);
        setTimeout(function () {
            clearTransition();
            if (drawerStarted) {
                return;
            }
            drawerElem.style.opacity = 0.001;
            drawerBg.style.visibility = "hidden";
            onClosed();
        }, s * 1000);
    }

    function toggleDrawer() {
        if (opened) {
            closeDrawer(0.225);
        } else {
            openDrawer(0.225);
        }
    }

    function onMovedNoOpen(e) {
        move(correct - e.touches[0].clientX, e);
    }

    function onMovedOpen(e) {
        move(startX - e.touches[0].clientX, e);
    }

    function onMovedNoOpenDesktop(e) {
        move(correct - e.clientX, e);
    }

    function onMovedOpenDesktop(e) {
        move(startX - e.clientX, e);
    }

    window.addEventListener("resize", function (e) {
        width = drawerElem.offsetWidth;
        if (!opened) {
            transfrom("translateX(-" + width + "px)");
        }
    });

    drawerElem.addEventListener(typeStart, function (e) {
        drawerElem.style.opacity = 1;
        drawerBg.style.visibility = "visible";
        startX = isMobile ? e.touches[0].clientX : e.clientX;
        startMoveTime = new Date();
        correct = width + startX;
        drawerStarted = true;
    });
    document.addEventListener(typeStart, function (e) {
        if (!drawerStarted) {
            return;
        }
        if (opened) {
            document.addEventListener(typeMove, isMobile ? onMovedOpen : onMovedOpenDesktop);
        } else {
            document.addEventListener(typeMove, isMobile ? onMovedNoOpen : onMovedNoOpenDesktop);
        }
    });

    document.addEventListener(typeEnd, function (e) {
        drawerStarted = false;
        stateMoved = false;
        if (!isMobile) {
            antiSelect.style.visibility = "hidden";
            document.body.classList.remove("rx_noselect");
        }
        document.removeEventListener(typeMove, isMobile ? onMovedOpen : onMovedOpenDesktop);
        document.removeEventListener(typeMove, isMobile ? onMovedNoOpen : onMovedNoOpenDesktop);

        speedSwipe = (((width / 2) / ((Math.abs((isMobile ? e.changedTouches[0].clientX : e.clientX) - startX)) / (new Date() - startMoveTime))) / 1000).toFixed(3);
        if (speedSwipe == Infinity) {
            if (!opened) {
                closeDrawer(0);
            } else {
                openDrawer(0);
            }
            return;
        }
        if (trx == 0) {
            return;
        }
        if (speedSwipe <= 0.150) {
            speedSwipe = 0.150;
        } else if (speedSwipe >= 0.5) {
            speedSwipe = 0.5;
        }
        var intent = (startX - (isMobile ? e.changedTouches[0].clientX : e.clientX)) > 0;
        if ((width / 2.25) > trx) {
            if (intent && speedSwipe < 0.4) {
                closeDrawer(speedSwipe);
            } else {
                openDrawer(speedSwipe);
            }
        } else {
            if (!intent && speedSwipe < 0.4) {
                openDrawer(speedSwipe);
            } else {
                closeDrawer(speedSwipe);
            }
        }
        trx = 0;
    });
    this.setDrawerIcon = function (icon) {
        drawerIcon = icon;
        drawerIcon.setOnClick(function (e) {
            toggleDrawer();
        });
    };
    this.getDrawerIcon = function () {
        return drawerIcon;
    };
    this.resetIconOnClick = function(){
        drawerIcon.setOnClick(function (e) {
            toggleDrawer();
        });
    };
    this.onOpenListener = function (listener) {
        onOpened = listener;
    };
    this.onCloseListener = function (listener) {
        onClosed = listener;
    };
    this.onMoveListener = function (listener) {
        onMove = listener;
    };
    this.openDrawer = function () {
        openDrawer();
    };
    this.closeDrawer = function () {
        closeDrawer();
    };
    this.toggleDrawer = function () {
        toggleDrawer();
    };
    this.isOpen = function () {
        return opened;
    };

    (function () {
        drawerBg = document.createElement("DIV");
        drawerBg.className = "drawer_bg";
        drawerBg.id = "drawer_bg";
        drawerElem.parentElement.insertBefore(drawerBg, drawerElem);
        drawerBg.onclick = function () {
            if (opened) {
                closeDrawer(0.225);
            }
        };
        antiSelect = document.createElement("DIV");
        antiSelect.className = "antiSelect";
        drawerElem.appendChild(antiSelect);
        var label = document.createElement("DIV");
        label.className = "label";
        drawerElem.appendChild(label);
        //Find prop name
        var vendors;
        if (antiSelect.style.transform === undefined) {
            vendors = ['Webkit', 'Moz', 'ms', 'O'];
            for (var vendor in vendors) {
                if (antiSelect.style[vendors[vendor] + 'Transform'] !== undefined) {
                    transformProp = vendors[vendor] + 'Transform';
                    propPrefixCss = "-" + vendors[vendor].toLowerCase() + "-";
                }
                if (antiSelect.style[vendors[vendor] + 'Transition'] !== undefined) {
                    transitionProp = vendors[vendor] + 'Transition';
                }
            }
        }
        if (/.*opera.*presto/i.test(navigator.userAgent)) {
            trZ = "";
        }
    })();
}

/* Hamburger Library */
function DrawerIcon(icon) {
    "use strict";
    var ic,
        line1,
        line2,
        line3,
        const1 = 1 / 300,
        const2 = 1 / 500,
        const3 = 2 / 3,
        direction = true,
        locked = false,
        rotateLine,
        scaleX,
        transY,
        transX,
        scaleX2,
        transX2,
        rotateIc,
        transformProp = "transform",
        transitionProp = "transition",
        trZ = "translateZ(0)",
        propPrefixCss = "";

    function setProperty(elem, property, value) {
        elem.style[property] = value;
    }

    function enableAnimation(duration) {
        var transition = propPrefixCss + "transform " + duration + "s ease";
        setProperty(line1, transitionProp, transition);
        setProperty(line2, transitionProp, transition);
        setProperty(line3, transitionProp, transition);
        setProperty(ic, transitionProp, transition);
    }

    function disableAnimation() {
        setProperty(line1, transitionProp, "none");
        setProperty(line2, transitionProp, "none");
        setProperty(line3, transitionProp, "none");
        setProperty(ic, transitionProp, "none");
    }
    
    this.state = function () {
        return direction;
    };
    
    this.setOnClick = function (listener) {
        icon.onclick = listener;
    };
    
    this.set = function (percent) {
        if (locked) {
            return;
        }
        if (percent > 100) {
            percent = 100;
        }
        if (percent < 0) {
            percent = 0;
        }
        if (percent >= 100) {
            direction = false;
        }
        if (percent <= 0) {
            direction = true;
        }

        rotateLine = 0.45 * percent;
        scaleX = 1 - const1 * percent;
        transY = 0.054 * percent;
        transX = 0.033 * percent;
        scaleX2 = 1 - const2 * percent;
        transX2 = -0.01 * percent;
        if (direction) {
            rotateIc = 1.80 * percent;
        } else {
            rotateIc = 360 - (1.80 * percent);
        }
        setProperty(line1, transformProp, "rotate(" + rotateLine + "deg) scaleX(" + scaleX + ") translateY(" + transY + "px) translateX(" + transX + "px) " + trZ);
        setProperty(line2, transformProp, "scaleX(" + scaleX2 + ") translateX(" + transX2 + "px) " + trZ);
        setProperty(line3, transformProp, "rotate(" + (-rotateLine) + "deg) scaleX(" + scaleX + ") translateY(" + (-transY) + "px) translateX(" + transX + "px) " + trZ);
        setProperty(ic, transformProp, "rotate(" + rotateIc + "deg) " + trZ);
    };
    
    this.setState = function (state, duration) {
        duration = duration || 0.225;
        enableAnimation(duration);
        var temp = this;
        switch (state) {
            case 0:
                this.set(1);
                break;
            case 1:
                this.set(100);
                break;
        }
        setTimeout(function () {
            disableAnimation();
            if (state === 0) {
                temp.set(0);
            }
        }, Number(duration) * 1000);
    };

    this.lock = function () {
        locked = true;
    };
    this.unLock = function () {
        locked = false;
    };

    (function () {
        icon.innerHTML += '<span class="ic"><i class="line one"></i><i class="line two"></i><i class="line thr"></i></span>';
        ic = icon.querySelector(".ic");
        line1 = ic.querySelector(".one");
        line2 = ic.querySelector(".two");
        line3 = ic.querySelector(".thr");
        //Find prop name
        var testEl = document.createElement('div'),
            vendors;
        if (testEl.style.transform === undefined) {
            vendors = ['Webkit', 'Moz', 'ms', 'O'];
            for (var vendor in vendors) {
                if (testEl.style[vendors[vendor] + 'Transform'] !== undefined) {
                    transformProp = vendors[vendor] + 'Transform';
                    propPrefixCss = "-" + vendors[vendor].toLowerCase() + "-";
                }
                if (testEl.style[vendors[vendor] + 'Transition'] !== undefined) {
                    transitionProp = vendors[vendor] + 'Transition';
                }
            }
        }
        if (/.*opera.*presto/i.test(navigator.userAgent)) {
            trZ = "";
        }
    })();
}
```

## License

Public domain: [http://unlicense.org](http://unlicense.org)
