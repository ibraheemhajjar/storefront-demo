<template>
  <div class="grid-container">
    <div v-for="product in products" :key="product.id">
      <nuxt-link class="product-container" :to="`/products/${product.id}`">
        <NuxtImg :src="product.images[0]" class="grid-img" />
        <h4 class="product-title">{{ product.title }}</h4>
        <p class="product-price">{{ "$" + product.price }}</p>
      </nuxt-link>
    </div>
  </div>
</template>

<script setup>
const products = [
  {
    id: 1,
    title: "Majestic Mountain Graphic T-Shirt",
    price: 39,
    description:
      "Elevate your wardrobe with this stylish black t-shirt featuring a striking monochrome mountain range graphic. Perfect for those who love the outdoors or want to add a touch of nature-inspired design to their look, this tee is crafted from soft, breathable fabric ensuring all-day comfort. Ideal for casual outings or as a unique gift, this t-shirt is a versatile addition to any collection.",
    images: [
      "https://i.imgur.com/QkIa5tT.jpeg",
      "https://i.imgur.com/jb5Yu0h.jpeg",
      "https://i.imgur.com/UlxxXyG.jpeg",
      "https://i.imgur.com/QkIa5tT.jpeg",
      "https://i.imgur.com/jb5Yu0h.jpeg",
      "https://i.imgur.com/UlxxXyG.jpeg",
      "https://i.imgur.com/QkIa5tT.jpeg",
      "https://i.imgur.com/jb5Yu0h.jpeg",
      "https://i.imgur.com/UlxxXyG.jpeg",
    ],
    creationAt: "2024-02-25T03:25:16.000Z",
    updatedAt: "2024-02-25T09:20:07.000Z",
    category: {
      id: 1,
      name: "Clothes",
      image: "https://i.imgur.com/QkIa5tT.jpeg",
      creationAt: "2024-02-25T03:25:16.000Z",
      updatedAt: "2024-02-25T03:25:16.000Z",
    },
  },
  {
    id: 2,
    title: "Classic Red Pullover Hoodie",
    price: 19,
    description:
      "Elevate your casual wardrobe with our Classic Red Pullover Hoodie. Crafted with a soft cotton blend for ultimate comfort, this vibrant red hoodie features a kangaroo pocket, adjustable drawstring hood, and ribbed cuffs for a snug fit. The timeless design ensures easy pairing with jeans or joggers for a relaxed yet stylish look, making it a versatile addition to your everyday attire.",
    images: [
      "https://i.imgur.com/1twoaDy.jpeg",
      "https://i.imgur.com/FDwQgLy.jpeg",
      "https://i.imgur.com/kg1ZhhH.jpeg",
    ],
    creationAt: "2024-02-25T03:25:16.000Z",
    updatedAt: "2024-02-25T09:28:47.000Z",
    category: {
      id: 1,
      name: "Clothes",
      image: "https://i.imgur.com/QkIa5tT.jpeg",
      creationAt: "2024-02-25T03:25:16.000Z",
      updatedAt: "2024-02-25T03:25:16.000Z",
    },
  },
  {
    id: 3,
    title: "Classic Heather Gray Hoodie",
    price: 90,
    description:
      "Stay cozy and stylish with our Classic Heather Gray Hoodie. Crafted from soft, durable fabric, it features a kangaroo pocket, adjustable drawstring hood, and ribbed cuffs. Perfect for a casual day out or a relaxing evening in, this hoodie is a versatile addition to any wardrobe.",
    images: [
      "https://i.imgur.com/cHddUCu.jpeg",
      "https://i.imgur.com/CFOjAgK.jpeg",
      "https://i.imgur.com/wbIMMme.jpeg",
    ],
    creationAt: "2024-02-25T03:25:16.000Z",
    updatedAt: "2024-02-25T09:57:32.000Z",
    category: {
      id: 1,
      name: "Clothes",
      image: "https://i.imgur.com/QkIa5tT.jpeg",
      creationAt: "2024-02-25T03:25:16.000Z",
      updatedAt: "2024-02-25T03:25:16.000Z",
    },
  },
  {
    id: 4,
    title: "Classic Grey Hooded Sweatshirt",
    price: 90,
    description:
      "Elevate your casual wear with our Classic Grey Hooded Sweatshirt. Made from a soft cotton blend, this hoodie features a front kangaroo pocket, an adjustable drawstring hood, and ribbed cuffs for a snug fit. Perfect for those chilly evenings or lazy weekends, it pairs effortlessly with your favorite jeans or joggers.",
    images: [
      "https://i.imgur.com/R2PN9Wq.jpeg",
      "https://i.imgur.com/IvxMPFr.jpeg",
      "https://i.imgur.com/7eW9nXP.jpeg",
    ],
    creationAt: "2024-02-25T03:25:16.000Z",
    updatedAt: "2024-02-25T03:25:16.000Z",
    category: {
      id: 1,
      name: "Clothes",
      image: "https://i.imgur.com/QkIa5tT.jpeg",
      creationAt: "2024-02-25T03:25:16.000Z",
      updatedAt: "2024-02-25T03:25:16.000Z",
    },
  },
  {
    id: 5,
    title: "Classic Black Hooded Sweatshirt",
    price: 79,
    description:
      "Elevate your casual wardrobe with our Classic Black Hooded Sweatshirt. Made from high-quality, soft fabric that ensures comfort and durability, this hoodie features a spacious kangaroo pocket and an adjustable drawstring hood. Its versatile design makes it perfect for a relaxed day at home or a casual outing.",
    images: [
      "https://i.imgur.com/cSytoSD.jpeg",
      "https://i.imgur.com/WwKucXb.jpeg",
    ],
    creationAt: "2024-02-25T03:25:16.000Z",
    updatedAt: "2024-02-25T09:59:44.000Z",
    category: {
      id: 1,
      name: "Clothes",
      image: "https://i.imgur.com/QkIa5tT.jpeg",
      creationAt: "2024-02-25T03:25:16.000Z",
      updatedAt: "2024-02-25T03:25:16.000Z",
    },
  },
  {
    id: 6,
    title: "Classic Comfort Fit Joggers",
    price: 25,
    description:
      "Discover the perfect blend of style and comfort with our Classic Comfort Fit Joggers. These versatile black joggers feature a soft elastic waistband with an adjustable drawstring, two side pockets, and ribbed ankle cuffs for a secure fit. Made from a lightweight and durable fabric, they are ideal for both active days and relaxed lounging.",
    images: [
      "https://i.imgur.com/ZKGofuB.jpeg",
      "https://i.imgur.com/GJi73H0.jpeg",
      "https://i.imgur.com/633Fqrz.jpeg",
    ],
    creationAt: "2024-02-25T03:25:16.000Z",
    updatedAt: "2024-02-25T03:25:16.000Z",
    category: {
      id: 1,
      name: "Clothes",
      image: "https://i.imgur.com/QkIa5tT.jpeg",
      creationAt: "2024-02-25T03:25:16.000Z",
      updatedAt: "2024-02-25T03:25:16.000Z",
    },
  },
  {
    id: 7,
    title: "Classic Comfort Drawstring Joggers",
    price: 79,
    description:
      "Experience the perfect blend of comfort and style with our Classic Comfort Drawstring Joggers. Designed for a relaxed fit, these joggers feature a soft, stretchable fabric, convenient side pockets, and an adjustable drawstring waist with elegant gold-tipped detailing. Ideal for lounging or running errands, these pants will quickly become your go-to for effortless, casual wear.",
    images: [
      "https://i.imgur.com/mp3rUty.jpeg",
      "https://i.imgur.com/JQRGIc2.jpeg",
    ],
    creationAt: "2024-02-25T03:25:16.000Z",
    updatedAt: "2024-02-25T03:25:16.000Z",
    category: {
      id: 1,
      name: "Clothes",
      image: "https://i.imgur.com/QkIa5tT.jpeg",
      creationAt: "2024-02-25T03:25:16.000Z",
      updatedAt: "2024-02-25T03:25:16.000Z",
    },
  },
  {
    id: 8,
    title: "Classic Red Jogger Sweatpants",
    price: 98,
    description:
      "Experience ultimate comfort with our red jogger sweatpants, perfect for both workout sessions and lounging around the house. Made with soft, durable fabric, these joggers feature a snug waistband, adjustable drawstring, and practical side pockets for functionality. Their tapered design and elastic cuffs offer a modern fit that keeps you looking stylish on the go.",
    images: [
      "https://i.imgur.com/9LFjwpI.jpeg",
      "https://i.imgur.com/vzrTgUR.jpeg",
      "https://i.imgur.com/p5NdI6n.jpeg",
    ],
    creationAt: "2024-02-25T03:25:16.000Z",
    updatedAt: "2024-02-25T03:25:16.000Z",
    category: {
      id: 1,
      name: "Clothes",
      image: "https://i.imgur.com/QkIa5tT.jpeg",
      creationAt: "2024-02-25T03:25:16.000Z",
      updatedAt: "2024-02-25T03:25:16.000Z",
    },
  },
  {
    id: 9,
    title: "Classic Navy Blue Baseball Cap",
    price: 61,
    description:
      "Step out in style with this sleek navy blue baseball cap. Crafted from durable material, it features a smooth, structured design and an adjustable strap for the perfect fit. Protect your eyes from the sun and complement your casual looks with this versatile and timeless accessory.",
    images: [
      "https://i.imgur.com/R3iobJA.jpeg",
      "https://i.imgur.com/Wv2KTsf.jpeg",
      "https://i.imgur.com/76HAxcA.jpeg",
    ],
    creationAt: "2024-02-25T03:25:16.000Z",
    updatedAt: "2024-02-25T03:25:16.000Z",
    category: {
      id: 1,
      name: "Clothes",
      image: "https://i.imgur.com/QkIa5tT.jpeg",
      creationAt: "2024-02-25T03:25:16.000Z",
      updatedAt: "2024-02-25T03:25:16.000Z",
    },
  },
  {
    id: 10,
    title: "Classic Blue Baseball Cap",
    price: 86,
    description:
      "Top off your casual look with our Classic Blue Baseball Cap, made from high-quality materials for lasting comfort. Featuring a timeless six-panel design with a pre-curved visor, this adjustable cap offers both style and practicality for everyday wear.",
    images: [
      "https://i.imgur.com/wXuQ7bm.jpeg",
      "https://i.imgur.com/BZrIEmb.jpeg",
      "https://i.imgur.com/KcT6BE0.jpeg",
    ],
    creationAt: "2024-02-25T03:25:16.000Z",
    updatedAt: "2024-02-25T03:25:16.000Z",
    category: {
      id: 1,
      name: "Clothes",
      image: "https://i.imgur.com/QkIa5tT.jpeg",
      creationAt: "2024-02-25T03:25:16.000Z",
      updatedAt: "2024-02-25T03:25:16.000Z",
    },
  },
];
</script>

<style>
.grid-container {
  width: 80%;
  max-width: 65rem;
  margin: 5rem auto;
  row-gap: 2rem;
  column-gap: 2rem;
  display: grid;
  align-items: stretch;
  justify-content: center;
  grid-template-columns: repeat(3, 1fr);
  text-align: center;
}

.product-container {
  text-decoration: none;
  width: 100%;
}

.grid-img {
  width: 100%;
}

.product-title {
  font-size: 1rem;
  color: #535353;
  margin-top: 1rem;
}
.product-price {
  font-size: 1rem;
  color: #929292;
  margin-top: 1rem;
}

@media (max-width: 768px) {
  .grid-container {
    grid-template-columns: repeat(2, 1fr);
  }
}
@media (max-width: 500px) {
  .grid-container {
    grid-template-columns: 1fr;
  }
}
</style>
