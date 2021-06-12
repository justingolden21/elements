---
layout: post
backLink: false
---

<!-- {:.inline-block .custom-underline-red .pt-10}
# Jekyll + Tailwind

{:.lead}
Minimal boilerplate for [Jekyll](https://jekyllrb.com/) sites and [Tailwind CSS](https://tailwindcss.com/). -->

<!-- arrow to scroll to top, accent underline to show page vertical progress -->

<!-- https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/rotate3d() -->
<!-- 1150 850 430 px -->
<style type="text/css">
#box-element {
	width: 170px;
	height: 230px;
    transform-style: preserve-3d;
    -webkit-animation: rotateBox 5s infinite;
    -moz-animation: rotateBox 5s infinite;
    animation: rotateBox 5s infinite;
	/*animation-play-state: paused;*/
}

#box-element:hover {
	/*animation-duration: 10s;*/
	/*animation-play-state: paused;*/
	/*animation-play-state: running;*/
}

#box-element:hover .face {
	box-shadow: 0px 0px 24px #f7941d99;
}

@-webkit-keyframes rotateBox { 100% { -webkit-transform: rotate3d(1, 1, 0, 360deg); } }
@-moz-keyframes rotateBox { 100% { -moz-transform: rotate3d(1, 1, 0, 360deg); } }
@keyframes rotateBox { 100% { transform: rotate3d(1, 1, 0, 360deg); } }

.face {
    width: 100%;
    height: 100%;
    position: absolute;
    backface-visibility: inherit;
    border: 2px solid white;

    filter: brightness(1.5);
}

.front, .back {
	width: 170px;
	height: 230px;
}
.right, .left {
	width: 86px;
	height: 230px;
}
.top, .bottom {
	width: 170px;
	height: 86px;
}

.front {
	background: url('assets/img/box/top.png') no-repeat center;
	background-size: contain;
    /*background: rgba(90,90,90,.7);*/
    transform: translateZ(43px);
}
.back {
	background: url('assets/img/box/bottom.png') no-repeat center;
	background-size: contain;
    /*background: rgba(0,210,0,.7);*/
    transform: rotateY(180deg) translateZ(43px);
}
.right {
	background: url('assets/img/box/long-right.png') no-repeat center;
	background-size: contain;
    /*background: rgba(210,0,0,.7);*/
    transform: rotateY(90deg) translateZ(126px); /*170-43=127, 126 works better though*/
}
.left {
	background: url('assets/img/box/long-left.png') no-repeat center;
	background-size: contain;
    /*background: rgba(0,0,210,.7);*/
    transform: rotateY(-90deg) translateZ(43px);
}
.top {
	background: url('assets/img/box/short-top.png') no-repeat center;
	background-size: contain;
    /*background: rgba(210,210,0,.7);*/
    transform: rotateX(90deg) translateZ(43px);
}
.bottom {
	background: url('assets/img/box/short-bottom.png') no-repeat center;
	background-size: contain;
    /*background: rgba(210,0,210,.7);*/
    transform: rotateX(-90deg) translateZ(186px); /*230-43=187, 186 works better though*/
}



#hero-text {
    animation: clipIn 2.5s linear;
    /*animation-delay: 1s;*/
    clip-path: polygon(0 0, 100% 0, 100% 0, 0 0);
    animation-fill-mode: forwards;
}
body {
    animation: fadeIn 1s linear;
    animation-fill-mode: forwards;
}
@keyframes clipIn {
    0% {
        clip-path: polygon(0 0, 100% 0, 100% 0, 0 0);
    }
    100% {
        /*has to be larger than 100% for descenders in type */
        clip-path: polygon(0 0, 100% 0, 100% 110%, 0% 110%);
    }
}
@keyframes fadeIn {
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
    }
}

</style>

<!-- replace box with still image for mobile? -->

<!-- 
design: gorgeous, sleek, minimal, modern design, hand crafted to create something that you can feel good about owning


articles
- what makes a good game
- testing a wide variety of audiences
- luck vs skill in game design
- user experience in game design

more
- tools (tracker, sample hand)
- print and play
- faq
- card gallery (search, sortable table, stats in charts)
- specs
- rules
- tracker
- testimonial/reviews/videos (quotes, articles, press, and more)
- branding guidelines
- about us / our story
- backers list

bottom:
- contact / enter email for maillist
- copyright with year
- socials

rotating card carousel early on page (between how to play and design)

rules page (separate has read online, print and play, faqs, link to youtube)

card gallery on mobile shows table/list and opens in modal with arrows or swipe to go back or next, permalink to cards

contact:
- btn to message on fb, or email

youtube:
how to play (3min)
basic strategy (3min)
advanced strategy (5min)
watch it played (8min)

page for variants: elements.website/variants, linked to in rules

insert images under gameplay and design

add more interesting btn icon hover effects (get users to click kickstarter btn)

use heroicons for non brands, download brand fontawesome icons

https://tailwindcomponents.com/component/toggle-switch

 -->

<section id="home">
  <br><br>
  <div class="flex md:flex-row flex-col items-center md:items-start">
    <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6 md:mb-0 mb-10 mt-10 items-center">
    	<div class="w-full text-center">
			<div id="box-element" class="inline-block">
				<div class="face front"></div>
				<div class="face back"></div>
				<div class="face right"></div>
				<div class="face left"></div>
				<div class="face top"></div>
				<div class="face bottom"></div>
			</div>
    	</div>
      <!-- <img class="object-cover object-center rounded" alt="hero" src="https://dummyimage.com/720x600"> -->
    </div>
    <div class="mx-2 lg:flex-grow md:w-1/2 lg:pl-8 md:pl-4 flex flex-col md:items-start md:text-left items-center text-center">
      <h1 id="hero-text" class="sm:text-3xl text-2xl mb-4" style="line-height: 1.25;"><span class="elements">ELEMENTS</span>
        <br class="hidden lg:inline-block">is a simple, speedy, spell-slinging party game
      </h1>
      <p class="mb-8 leading-relaxed font-thin text-left"><b class="dropcap">T</b>ake part in a one-of-a-kind battle royale experience for 2-8 players. Play begins by dealing 4 cards to each player. Players pick 1 card to keep and pass the remaining cards. Once players have selected their hands, they battle it out by casting the spells they selected to blast their enemies with fire, heal with water, craft gems, or counter or reflect the opposition with electricity. Win by being the last one standing, or reaching 20 gems first; the choice is yours. <br><a href=""><i class="fab fa-youtube"></i> Learn to play in 3 min.</a></p>
      <div class="flex justify-center">
        <!-- <button class="inline-flex text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-lg">Button</button> -->
        <!-- <button class="ml-4 inline-flex text-gray-400 bg-gray-800 border-0 py-2 px-6 focus:outline-none hover:bg-gray-700 hover:text-white rounded text-lg">Button</button> -->
        <button class="btn m-2 kickstarter"><i class="fab fa-kickstarter-k"></i> <br>Kickstarter</button>
        <!-- <button class="btn m-2"><i class="fas fa-book-open"></i> <br>Learn More</button> -->
        <button class="btn m-2"><i class="fas fa-share"></i> <br>Share</button>
      </div>
    </div>
  </div>
</section>

<section id="gameplay" class="mx-4">
	<br>
	<hr>
	<h1 class="text-center sm:text-3xl text-2xl mb-4">Gameplay</h1>

  <div class="flex md:flex-row flex-col items-start">
    <div class="md:w-1/2 max-w-xl">
        <img class="rules-img hide" src="assets/img/gameplay/trackers_clips.svg">
    </div>
    <div class="md:w-1/2 md:pl-4 flex flex-col">
        <p><b>Life and Gems</b></p>
        <p class="mb-8 leading-relaxed font-thin text-left"><b class="dropcap">E</b>ach player starts with 20 life and 0 gems. If you reach 20 gems, you win the game. If you run out of life, you lose the game. Be the last one standing or the first to 20 gems to claim victory.</p>
    </div>
  </div>
  <div class="flex md:flex-row flex-col items-start">
    <div class="md:w-1/2 md:pl-4 flex flex-col">
        <p><b>The Four Elements</b></p>
        <p class="mb-8 leading-relaxed font-thin text-left"><b class="dropcap">T</b>he Elements deck is a deck of 80 spells. There are four elements: fire, water, gem, and electric. Fire spells deal damage. Water spells heal damage. Gem spells craft gems. Electric spells counter other spells. Master the elements to emerge victorious. Each spell has a power and a target. The power determines the size of the effect, and the target determines who is affected.</p>
    </div>
    <div class="md:w-1/2 max-w-xl">
        <img class="rules-img hide" src="assets/img/gameplay/all_elements.svg">
    </div>
  </div>
  <div class="flex md:flex-row flex-col items-start">
    <div class="md:w-1/2 max-w-xl">
        <img class="rules-img hide" src="assets/img/gameplay/mechanics.svg">
    </div>
    <div class="md:w-1/2 md:pl-4 flex flex-col">
        <p><b>Combining and Overpowering</b></p>
        <p class="mb-8 leading-relaxed font-thin text-left"><b class="dropcap">Y</b>ou can combine and overpower spells of the same element type. You may combine multiple spells of the same element into a single spell. When doing this, combine their power and select any target from among those spells. You may overpower a spell by responding immediately after it was cast by casting another spell of the same element type and greater power. This negates the previous spell and casts your spell.</p>
    </div>
  </div>
  <div class="flex md:flex-row flex-col items-start">
    <div class="md:w-1/2 md:pl-4 flex flex-col">
        <p><b>Round Structure</b></p>
        <p class="mb-8 leading-relaxed font-thin text-left"><b class="dropcap">E</b>ach round, players select spells, then take turns casting one spell per turn or passing the turn. When all players have passed the turn in a row, the round ends and a new round begins. Rounds continue until a player wins the game. <br><br> During selection, each player sets aside their previous hand, then draws 4 cards. They chose 2 to keep and 2 to pass (clockwise). Players then combine these cards with their previous hand, and discard down to 4 cards. After selection, players cast their spells. Each player may cast up to one spell per turn.</p>
    </div>
    <div class="md:w-1/2 max-w-xl">
        <img class="rules-img hide" src="assets/img/gameplay/keep_pass.svg">
    </div>
  </div>
  <div class="flex md:flex-row flex-col items-start">
    <div class="md:w-1/2 max-w-xl">
        <img class="rules-img hide" src="assets/img/gameplay/great_spells.svg">
    </div>
    <div class="md:w-1/2 md:pl-4 flex flex-col">
        <p><b>Great Spells</b></p>
        <p class="mb-8 leading-relaxed font-thin text-left"><b class="dropcap">A</b>fter selection, players can elect to purchase a Great Spell for 8 gems. A player can only purchase one Great Spell per game. Great Spells do not take up hand space.</p>
    </div>
  </div>
  <p>Games are fast-paced and exciting, with each player trying to anticipate their opponents and adapt their strategy as the game evolves. Utilize your resources efficiently, predict your opponents, and select the right cards to survive.</p>
  <details class="text-sm font-thin"><summary>Footnotes</summary> Determining who goes first: Randomly determine the starting player for the first round. Future rounds start with the first player to pass.<br><br>Discarding: players secretly discard, then reveal their discarded cards.<br><br>Running out of cards: If the deck runs out of cards, shuffle the discard pile into the deck.<br><br>Ties: If multiple players reach 20 gems at the same time, the player with the greatest gem total wins. If there is a tie, the player with the greatest life wins. If there is a tie, the current player wins. If multiple players reach 0 life at the same time, players lose clockwise starting with the caster.<br><br>Priority for responding to spells: priority for responding to spells goes clockwise starting from the caster. If a player responds, priority for responding to that goes clockwise from the player who cast the response. Spells can only affect the most recently cast spell.<br><br>Great Spells: Great Spells are revealed. A player cannot purchase a Great Spell another player controls. Upon casting a Great Spell, the player then returns it to the center. If a player loses the game, their Great Spell returns to the center. Priority for purchasing a Great Spell goes clockwise starting with the player who will start the round (the player who passed first).</details>
</section>

<!-- todo: animate other diagrams on scroll -->

<section id="design" class="mx-4">
	<br>
	<hr>
	<h1 class="text-center sm:text-3xl text-2xl mb-4">Design</h1>

    <div class="w-96 mx-auto">
    <svg id="animated-cardback" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 180 252">
    <style>
    .cls-1,.cls-55{fill:#000;}
    .cls-2{font-size:24px;fill:#fff;font-family:Arvo;letter-spacing:0.1em;}
    .cls-3,.cls-8,.cls-9{fill:none;}
    .cls-3,.cls-5,.cls-8,.cls-9{stroke:#fff;}
    .cls-3,.cls-5,.cls-8{stroke-linecap:round;stroke-linejoin:round;}
    .cls-3,.cls-5,.cls-8,.cls-9{stroke-width:2.25px;}

    circle:not(#bigCircle) {
      animation: drawSmall 2s ease-in-out 0s forwards;
      animation-delay: 3s;
      stroke-dasharray:50;
      stroke-dashoffset:50;
      fill: none;

      animation-play-state: paused;
    }
    #fire {
      animation: drawMed 4s ease-in-out 0s forwards;
      stroke-dasharray:200;
      stroke-dashoffset:200;
      fill: none;

      animation-play-state: paused;
    }
    ellipse {
      animation: drawBig 5s ease-in-out 0s forwards;
      stroke-dasharray:500;
      stroke-dashoffset:0;
      fill: none;

      animation-play-state: paused;
    }
    text, #border {
      animation: fadeIn 2s ease-in-out 0s forwards;
      animation-delay: 3.5s;
      opacity: 0;

      animation-play-state: paused;
    }

    @keyframes drawSmall {
      0% {
        stroke-dashoffset: 50;
        opacity: 0;
        fill:#000;
      }
      100% {
        stroke-dashoffset: 0;
        fill:#000;
        opacity: 1;
      }
    }
    @keyframes drawMed {
      0% {
        stroke-dashoffset: 200;
        opacity: 0;
        fill:#000;
      }
      100% {
        stroke-dashoffset: 0;
        fill:#000;
        opacity: 1;
      }
    }
    @keyframes drawBig {
      0% {
        stroke-dashoffset: 500;
        opacity: 0;
      }
      100% {
        stroke-dashoffset: 0;
        opacity: 1;
      }
    }

    @keyframes fadeIn {
      0% {
        opacity: 0;
      }
      100% {
        opacity: 1;
      }
    }
    </style>
    <rect class="cls-1" width="180" height="252"/>
    <text class="cls-2" transform="translate(17.39 225.23) scale(0.95 1)">ELEMENTS</text>

    <ellipse class="cls-3" cx="90" cy="108" rx="27" ry="81"/>
    <ellipse class="cls-3" cx="90" cy="108" rx="81" ry="27" transform="translate(-41.94 59.47) rotate(-30)"/>
    <ellipse class="cls-3" cx="90" cy="108" rx="27" ry="81" transform="translate(-48.53 131.94) rotate(-60)"/>

    <circle id="bigCircle" class="cls-1" cx="90" cy="108" r="36"/>
    <circle class="cls-5" cx="43.23" cy="62.08" r="4.5"/>
    <circle class="cls-5" cx="153.47" cy="90.31" r="4.5"/>
    <circle class="cls-5" cx="74.05" cy="171.55" r="4.5"/>
    <path id="fire" class="cls-8" d="M86.69,76.31c2.06.37,11.78,6.37,13.58,26.54a0,0,0,0,0,0,0c1.51-.44,3.68-4.9,1.62-11.41,0,0,0-.08,0,0,2.65,2.76,11.81,13.58,3.57,23.48v0c.18.74,2.39,1.73,3.71-.81,0,0,.08,0,.08,0-1.18,32.62-51.28,20.62-37.33-9.64,5.89-11.08,17.34-4,14.65-28.16C86.62,76.35,86.65,76.31,86.69,76.31Z"/>

    <rect id="border" class="cls-9" x="9" y="9" width="162" height="234"/>
    </svg>
    </div>

    <script type="text/javascript">
    // https://stackoverflow.com/a/46985264/4907950
    const svgLocation = document.getElementById('animated-cardback').getBoundingClientRect();
    const offsetToTriggerAnimation = svgLocation.y + svgLocation.height;

    function scrollAnimTriggerCheck(evt) {
        if(window.scrollY + window.innerHeight > offsetToTriggerAnimation) {
            document.querySelectorAll('#animated-cardback *').forEach(elm => elm.style.animationPlayState = 'running');
            document.removeEventListener('scroll', scrollAnimTriggerCheck);
        }
    }

    document.addEventListener('scroll', scrollAnimTriggerCheck);

    // ---- rules images ----

    const ruleImgs = document.querySelectorAll('.rules-img');
    let scrollChecks = [];
    for(let i=0; i<ruleImgs.length; i++) {
        const svgLoc = ruleImgs[i].getBoundingClientRect();
        const offsetAnim = svgLoc.y + svgLoc.height;
        scrollChecks.push(evt => {
            if(window.scrollY + window.innerHeight > offsetAnim) {
                ruleImgs[i].classList.remove('hide');
                ruleImgs[i].classList.add('show');
                document.removeEventListener('scroll', scrollChecks[i]);
            }
        });
        document.addEventListener('scroll', scrollChecks[i]);
    };
    </script>

	<p class="mb-8 leading-relaxed font-thin text-left"><b class="dropcap">L</b>orem ipsum dolor sit amet, consectetur adipiscing elit. Nullam nec sollicitudin turpis. Integer congue faucibus ipsum, non commodo odio porta id. Praesent magna ipsum, tincidunt at viverra non, sollicitudin ut neque. Donec id erat nec erat interdum blandit vitae eget nulla. Nam porttitor condimentum ipsum id sollicitudin. Sed ac diam sed mi rutrum tincidunt. Ut vitae venenatis dolor. Quisque et interdum nunc, eu malesuada sem. Quisque volutpat dui sit amet ante pretium, quis finibus urna sagittis. Vivamus lorem justo, consequat imperdiet ullamcorper sed, tristique vel lacus. Vivamus est quam, dictum eget arcu dictum, vulputate cursus urna. Vivamus porta nisi arcu, ac tempus turpis tempus ac. Sed in quam mauris. Praesent dolor risus, aliquam eu nulla eget, semper porta dolor. Curabitur ut diam feugiat, tristique libero at, suscipit nunc.</p>
</section>

<!-- ## Pages

<content class="grid md:grid-cols-2 gap-4">
    <a href="{% post_url 2020-01-01-demo %}" class="flex items-center justify-center space-x-2 w-full text-center py-5 px-6 bg-gray-500 hover:bg-blue-500 rounded shadow whitespace-nowrap">
        <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20"><path d="M5 4a2 2 0 012-2h6a2 2 0 012 2v14l-5-2.5L5 18V4z"></path></svg>
        <span>Demo article</span>
    </a>
    
</content>

<button class="btn">Hello There</button> 

---

-->
