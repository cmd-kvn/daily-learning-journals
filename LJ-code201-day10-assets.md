<header>
  <nav>
    <img src="http://placehold.it/200x70">
    <ul>
      <li>Nav Item 1</li>
      <li>Nav Item 2</li>
      <li>Nav Item 3</li>
      <li>Nav Item 4</li>
    </ul>
  </nav>
</header>
<main>
  <img src="http://placehold.it/960x450">
  <ul class="sub_banner clearfix">
    <li><img src="http://placehold.it/300x375"></li>
    <li><img src="http://placehold.it/300x375"></li>
    <li><img src="http://placehold.it/300x375"></li>
  </ul>
  <div class="featured_banner">
     <img src="http://placehold.it/480x375">
  </div>
  <h2>Featured Section Heading</h2>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quae, sunt at voluptate magnam debitis commodi dolorum odio perferendis dignissimos, quod aliquam totam praesentium reiciendis mollitia exercitationem nobis laudantium voluptatum delectus!
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi velit, numquam error fugit quo, nobis. Doloribus odit, reprehenderit saepe nobis, enim sunt esse eos natus distinctio, illum, voluptate ex odio
    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi velit, numquam error fugit quo, nobis. Doloribus odit, reprehenderit saepe nobis, enim sunt esse eos natus distinctio, illum, voluptate ex odio?
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi velit, numquam error fugit quo, nobis. Doloribus odit, reprehenderit saepe nobis, enim sunt esse eos natus distinctio, illum, voluptate ex odio?
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi velit, numquam error fugit quo, nobis. Doloribus odit, reprehenderit saepe nobis, enim sunt esse eos natus distinctio, illum, voluptate ex odio?
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi velit, numquam error fugit quo, nobis. Doloribus odit, reprehenderit saepe nobis, enim sunt esse eos natus distinctio, illum, voluptate ex odio?
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi velit, numquam error fugit quo, nobis. Doloribus odit, reprehenderit saepe nobis, enim sunt esse eos natus distinctio, illum, voluptate ex odio?
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi velit, numquam error fugit quo, nobis. Doloribus odit, reprehenderit saepe nobis, enim sunt esse eos natus distinctio, illum, voluptate ex odio?</p>
  <button>Call to Action</button>
</main>
<footer></footer>

////////////////////////////////////////////////////////////////////

body {
  font-family: helvetica;
}

header {
  background-color: #888;
}

nav {
  width: 960px;
  margin: 0 auto; /* center content */
}

nav img {
  float: left;
}

nav ul li {
  display: inline; /*   inline elements can't be positioned vertically, do it with inline-block */
  margin-left: 100px;
}

nav ul {
  display: inline-block;
  margin: 27px 0; /* top margin needs to take the size of the header   */
}

main {
  width: 960px;
  margin: 30px auto; /*   center block level elements by setting the width and zero/autoing the margin */
}

.sub_banner {
  margin-top: 30px;
/*   margin-bottom: 435px; */
/*   375(image height) + x = 435 */
}

.sub_banner li {
  float: left;
  margin-left: 30px;
}

.sub_banner li:first-child {
/*   first-child in this case is the first 300x375 */
  margin-left: 0px;
}

/* .sub_banner li img {
  margin-bottom: 30px;
/*   hacky fix
} */

.featured_banner {
  float: left;
  margin-right: 30px;
}

main h2 {
  font-size: 25px;
  text-align: center;
}

main p {
  margin: 30px 0;
  height: 250px;
  overflow: auto;
}

main button {
  border: none;
  width: 230px;
  padding: 10px 40px;
  font-size: 15px;
  border-radius: 10px;
  cursor: pointer;
  margin: 0 auto;
  display: block;
}

footer {
  background-color: #888;
  height: 70px;
}

.clearfix:after {
  display: table;
  content: '';
  clear: both;
/*   pseudo-child 'after' is setting content to the page. Puts a secret extra element as the last child and sets property as clear:both */
}
