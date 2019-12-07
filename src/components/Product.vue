
<template>
  <div>
	  <h2 style="display: block">Buy me a {{ product }}</h2>

	  <div class="product">-
	    <div>
	      <img style="display: block" src="../../public/seth-weisfeld-510833-unsplash.jpg" >
	      <a style="background-color:black;color:white;text-decoration:none;padding:4px 6px;font-family:-apple-system, BlinkMacSystemFont, &quot;San Francisco&quot;, &quot;Helvetica Neue&quot;, Helvetica, Ubuntu, Roboto, Noto, &quot;Segoe UI&quot;, Arial, sans-serif;font-size:12px;font-weight:bold;line-height:1.2;display:inline-block;border-radius:3px"
	         href="https://unsplash.com/@jackharner?utm_medium=referral&amp;utm_campaign=photographer-credit&amp;utm_content=creditBadge"
	         target="_blank" rel="noopener noreferrer"
	         title="Download free do whatever you want high-resolution photos from Jack Harner">

	         <span style="display:inline-block;padding:2px 3px">
	           <svg xmlns="http://www.w3.org/2000/svg" style="height:12px;width:auto;position:relative;vertical-align:middle;top:-2px;fill:white" viewBox="0 0 32 32">
	             <title>unsplash-logo</title>
	             <path d="M10 9V0h12v9H10zm12 5h10v18H0V14h10v9h12v-9z"></path>
	           </svg>
	        </span>
	        <span style="display:inline-block;padding:2px 3px">
	          Jack Harner
	        </span>
	      </a>
	    </div>
			<div>
		    <p v-if="isHalfEmpty">Glass is half empty</p>
		    <p v-else>Glass is half full</p>
				<p>All the beers:</p>
				<ul>
					<li v-for="variant in variants" :key="variant.id">{{ variant.name }}</li>
				</ul>
			</div>
	  </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      product: 'beer',
      isHalfEmpty: true,
      variants: [
        { id: 1,
					name: "IPA" },
        { id: 2,
					name: "Brown Ale" },
        { id: 3,
					name: "Stout" },
        { id: 4,
					name: "Red Ale" },
        { id: 5,
					name: "Brown" },
        { id: 6,
					name: "Dunkle" },
        { id: 7,
					name: "Oktoberfest" },
        { id: 8,
					name: "Hefeveizen" },
        { id: 9,
					name: "Porter" }
      ]
    }
  }
}
</script>

<style scoped>
body {
  color: #282828;
  margin: 0px;
}

button {
  margin-top: 30px;
  border: none;
  background-color: #1E95EA;
  color: white;
  height: 40px;
  width: 100px;
  font-size: 14px;
}

img {
  border: 1px solid #d8d8d8;
  width: 70%;
  margin: 0;
  padding: 0;
  box-shadow: 0px .5px 1px #d8d8d8;
}

input {
  width: 100%;
  height: 25px;
  margin-bottom: 20px;
}

textarea {
  width: 100%;
  height: 60px;
}

.activeTab {
  color: #16C0B0;
  text-decoration: underline;
}

.color-box {
  width: 40px;
  height: 40px;
  margin-top: 5px;
}

.cart {
  margin-right: 25px;
  border: 1px solid #d8d8d8;
  padding: 5px 20px;
}

.disabledButton {
  background-color: #d8d8d8;
}

.product {
  padding: 1rem;
}

.product-image {
  height: 2rem;
  border-radius: 5px;
}

.product-image,
.product-info {
  margin-top: 10px;
  width: 50%;
}

.review-form {
  width: 400px;
  padding: 20px;
  margin: 40px;
  border: 1px solid #d8d8d8;
}

.tab {
  margin-left: 20px;
  cursor: pointer;
}
</style>
