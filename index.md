---
layout: post
backLink: false
---

<!-- {:.inline-block .custom-underline-red .pt-10}
# Jekyll + Tailwind

{:.lead}
Minimal boilerplate for [Jekyll](https://jekyllrb.com/) sites and [Tailwind CSS](https://tailwindcss.com/). -->

  <!-- <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r83/three.min.js"></script> -->

<!-- <img src="assets/img/animated cardback.svg" class="w-32"> -->



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

</style>

<!-- replace box with still image for mobile? -->

<!-- 
design: gorgeous, sleek, minimal, modern design, hand crafted to create something that you can feel good about owning


articles
- what makes a good game
- testing a wide variety of audiences

more
- tools (tracker, sample hand)
- print and play
- faq
- card gallery (search, sortable table, stats in charts)
- specs
- rules
- tracker
- testimonial/reviews/videos
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

https://tailwindcomponents.com/component/toggle-switch

 -->

<section id="home">
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
    <div class="mx-4 lg:flex-grow md:w-1/2 lg:pl-16 md:pl-8 flex flex-col md:items-start md:text-left items-center text-center">
      <h1 class="sm:text-3xl text-2xl mb-4"><span style="font-family: Arvo; font-weight: normal;" class="tracking-widest">ELEMENTS</span>
        <br class="hidden lg:inline-block">is a simple, speedy, spell-slinging party game
      </h1>
      <p class="mb-8 leading-relaxed font-thin text-left">Take part in a one-of-a-kind battle royale experience for 2-8 players. Play begins by dealing 4 cards to each player. Players pick 1 card to keep and pass the remaining cards. Once players have selected their hands, they battle it out by casting the spells they selected to blast their enemies with fire, heal with water, craft gems, or counter or reflect the opposition with electricity. Win by being the last one standing, or reaching 20 gems first; the choice is yours. <br><a href=""><i class="fab fa-youtube"></i> Learn to play in 3 min.</a></p>
      <div class="flex justify-center">
        <!-- <button class="inline-flex text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-lg">Button</button> -->
        <!-- <button class="ml-4 inline-flex text-gray-400 bg-gray-800 border-0 py-2 px-6 focus:outline-none hover:bg-gray-700 hover:text-white rounded text-lg">Button</button> -->
        <button class="btn kickstarter"><i class="fab fa-kickstarter"></i> Kickstarter</button>
        <button class="btn"><i class="fas fa-book-open"></i> Learn More</button>
      </div>
    </div>
  </div>
</section>

<hr>

<section id="gameplay" class="mx-4">
	<h1 class="text-center sm:text-3xl text-2xl mb-4">Gameplay</h1>
	<p class="mb-8 leading-relaxed font-thin text-left">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam nec sollicitudin turpis. Integer congue faucibus ipsum, non commodo odio porta id. Praesent magna ipsum, tincidunt at viverra non, sollicitudin ut neque. Donec id erat nec erat interdum blandit vitae eget nulla. Nam porttitor condimentum ipsum id sollicitudin. Sed ac diam sed mi rutrum tincidunt. Ut vitae venenatis dolor. Quisque et interdum nunc, eu malesuada sem. Quisque volutpat dui sit amet ante pretium, quis finibus urna sagittis. Vivamus lorem justo, consequat imperdiet ullamcorper sed, tristique vel lacus. Vivamus est quam, dictum eget arcu dictum, vulputate cursus urna. Vivamus porta nisi arcu, ac tempus turpis tempus ac. Sed in quam mauris. Praesent dolor risus, aliquam eu nulla eget, semper porta dolor. Curabitur ut diam feugiat, tristique libero at, suscipit nunc.</p>
</section>

<hr>

<section id="design" class="mx-4">
	<h1 class="text-center sm:text-3xl text-2xl mb-4">Design</h1>
	<p class="mb-8 leading-relaxed font-thin text-left">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam nec sollicitudin turpis. Integer congue faucibus ipsum, non commodo odio porta id. Praesent magna ipsum, tincidunt at viverra non, sollicitudin ut neque. Donec id erat nec erat interdum blandit vitae eget nulla. Nam porttitor condimentum ipsum id sollicitudin. Sed ac diam sed mi rutrum tincidunt. Ut vitae venenatis dolor. Quisque et interdum nunc, eu malesuada sem. Quisque volutpat dui sit amet ante pretium, quis finibus urna sagittis. Vivamus lorem justo, consequat imperdiet ullamcorper sed, tristique vel lacus. Vivamus est quam, dictum eget arcu dictum, vulputate cursus urna. Vivamus porta nisi arcu, ac tempus turpis tempus ac. Sed in quam mauris. Praesent dolor risus, aliquam eu nulla eget, semper porta dolor. Curabitur ut diam feugiat, tristique libero at, suscipit nunc.</p>
</section>




<!-- 
<script type="text/javascript">

// https://threejs.org/docs/#api/en/textures/CubeTexture
// https://medium.com/@necsoft/three-js-101-hello-world-part-1-443207b1ebe1

let scene = new THREE.Scene();

let camera = new THREE.PerspectiveCamera(75, window.innerWidth/window.innerHeight, 0.1, 1000);
camera.position.z = 4;

let renderer = new THREE.WebGLRenderer({antialias:true});
renderer.setClearColor('#000');
renderer.setSize(window.innerWidth, window.innerHeight);

document.body.appendChild(renderer.domElement);

// ------------------------------------------------

// const loader = new THREE.CubeTextureLoader();
// loader.setPath('assets/img/box/');
// const textureCube = loader.load([
// 	'top.png', 'bottom.png',
// 	'long-left.png', 'long-right.png',
// 	'short-bottom.png', 'short-top.png'
// ]);
// textureCube.minFilter = THREE.LinearFilter; // or NearestFilter https://stackoverflow.com/questions/29421702/threejs-texture


let loader = new THREE.TextureLoader();
loader.setPath('assets/img/box/');
// https://stackoverflow.com/questions/35877484/three-js-using-cubetextureloader-to-create-a-different-image-on-each-face-of-a
let materials = [
    new THREE.MeshBasicMaterial( { map: loader.load("top.png") } ),
    new THREE.MeshBasicMaterial( { map: loader.load("bottom.png") } ),
    new THREE.MeshBasicMaterial( { map: loader.load("long-right.png") } ),
    new THREE.MeshBasicMaterial( { map: loader.load("long-left.png") } ),
    new THREE.MeshBasicMaterial( { map: loader.load("short-top.png") } ),
    new THREE.MeshBasicMaterial( { map: loader.load("short-bottom.png") } ),
];


const geometry = new THREE.BoxGeometry(1, 0.7, 0.5);
const material = new THREE.MeshBasicMaterial( { color: '#433F81', /*envMap: textureCube*/ } );
let cube = new THREE.Mesh(geometry, materials);

scene.add(cube);

const render = ()=> {
	requestAnimationFrame(render);
	cube.rotation.x += 0.01;
	cube.rotation.y += 0.01;

	renderer.render(scene, camera);
};
render();
</script>

 -->


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
 


