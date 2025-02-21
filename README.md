import React, { useState } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { ShoppingCart } from "lucide-react";

const products = [
  { id: 1, name: "Vêtements", price: 50, image: "https://via.placeholder.com/150" },
  { id: 2, name: "Chaussures", price: 80, image: "https://via.placeholder.com/150" },
  { id: 3, name: "Plantes", price: 30, image: "https://via.placeholder.com/150" },
  { id: 4, name: "Mèches", price: 25, image: "https://via.placeholder.com/150" },
  { id: 5, name: "Accessoires", price: 15, image: "https://via.placeholder.com/150" },
  { id: 6, name: "Beauté", price: 40, image: "https://via.placeholder.com/150" }
];

export default function Shop() {
  const [cart, setCart] = useState([]);

  const addToCart = (product) => {
    setCart([...cart, product]);
  };

  return (
    <div className="p-6">
      <h1 className="text-3xl font-bold mb-4">Boutique en ligne</h1>
      <div className="grid grid-cols-3 gap-4">
        {products.map((product) => (
          <Card key={product.id} className="p-4 text-center">
            <img src={product.image} alt={product.name} className="mb-2 mx-auto" />
            <h2 className="text-lg font-semibold">{product.name}</h2>
            <p className="text-gray-600">${product.price}</p>
            <Button className="mt-2" onClick={() => addToCart(product)}>
              Ajouter au panier
            </Button>
          </Card>
        ))}
      </div>
      <div className="mt-6 p-4 border rounded-md">
        <h2 className="text-xl font-bold mb-2 flex items-center">
          <ShoppingCart className="mr-2" /> Panier
        </h2>
        {cart.length === 0 ? (
          <p>Votre panier est vide.</p>
        ) : (
          <ul>
            {cart.map((item, index) => (
              <li key={index} className="flex justify-between py-1">
                {item.name} - ${item.price}
              </li>
            ))}
          </ul>
        )}
      </div>
      <div className="mt-6 p-4 border rounded-md">
        <h2 className="text-xl font-bold mb-2">Contactez-nous</h2>
        <form>
          <div className="mb-2">
            <label className="block text-sm font-medium">Nom</label>
            <input type="text" className="w-full p-2 border rounded-md" placeholder="Votre nom" />
          </div>
          <div className="mb-2">
            <label className="block text-sm font-medium">Email</label>
            <input type="email" className="w-full p-2 border rounded-md" placeholder="Votre email" />
          </div>
          <div className="mb-2">
            <label className="block text-sm font-medium">Message</label>
            <textarea className="w-full p-2 border rounded-md" placeholder="Votre message"></textarea>
          </div>
          <Button type="submit" className="mt-2">Envoyer</Button>
        </form>
      </div>
    </div>
  );
}
import React, { useState } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { ShoppingCart } from "lucide-react";

const products = [
  { id: 1, name: "Vêtements", price: 50, image: "https://via.placeholder.com/150" },
  { id: 2, name: "Chaussures", price: 80, image: "https://via.placeholder.com/150" },
  { id: 3, name: "Plantes", price: 30, image: "https://via.placeholder.com/150" },
  { id: 4, name: "Mèches", price: 25, image: "https://via.placeholder.com/150" },
  { id: 5, name: "Accessoires", price: 15, image: "https://via.placeholder.com/150" },
  { id: 6, name: "Beauté", price: 40, image: "https://via.placeholder.com/150" }
];

export default function Shop() {
  const [cart, setCart] = useState([]);

  const addToCart = (product) => {
    setCart([...cart, product]);
  };

  return (
    <div className="p-6">
      <h1 className="text-3xl font-bold mb-4">Boutique en ligne</h1>
      <div className="grid grid-cols-3 gap-4">
        {products.map((product) => (
          <Card key={product.id} className="p-4 text-center">
            <img src={product.image} alt={product.name} className="mb-2 mx-auto" />
            <h2 className="text-lg font-semibold">{product.name}</h2>
            <p className="text-gray-600">${product.price}</p>
            <Button className="mt-2" onClick={() => addToCart(product)}>
              Ajouter au panier
            </Button>
          </Card>
        ))}
      </div>
      <div className="mt-6 p-4 border rounded-md">
        <h2 className="text-xl font-bold mb-2 flex items-center">
          <ShoppingCart className="mr-2" /> Panier
        </h2>
        {cart.length === 0 ? (
          <p>Votre panier est vide.</p>
        ) : (
          <ul>
            {cart.map((item, index) => (
              <li key={index} className="flex justify-between py-1">
                {item.name} - ${item.price}
              </li>
            ))}
          </ul>
        )}
      </div>
      <div className="mt-6 p-4 border rounded-md">
        <h2 className="text-xl font-bold mb-2">Contactez-nous</h2>
        <form>
          <div className="mb-2">
            <label className="block text-sm font-medium">Nom</label>
            <input type="text" className="w-full p-2 border rounded-md" placeholder="Votre nom" />
          </div>
          <div className="mb-2">
            <label className="block text-sm font-medium">Email</label>
            <input type="email" className="w-full p-2 border rounded-md" placeholder="Votre email" />
          </div>
          <div className="mb-2">
            <label className="block text-sm font-medium">Message</label>
            <textarea className="w-full p-2 border rounded-md" placeholder="Votre message"></textarea>
          </div>
          <Button type="submit" className="mt-2">Envoyer</Button>
        </form>
      </div>
    </div>
  );
}


<!--
  <<< Author notes: Course header >>>
  Include a 1280×640 image, course title in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Add your open source license, GitHub uses MIT license.
-->

# GitHub Pages

_Create a site or blog from your GitHub repositories with GitHub Pages._

</header>

<!--
  <<< Author notes: Course start >>>
  Include start button, a note about Actions minutes,
  and tell the learner why they should take the course.
-->

## Welcome

With GitHub Pages, you can host project blogs, documentation, resumes, portfolios, or any other static content you'd like. Your GitHub repository can easily become its own website. In this course, we'll show you how to set up your own site or blog using GitHub Pages.

- **Who is this for**: Beginners, students, project maintainers, small businesses.
- **What you'll learn**: How to build a GitHub Pages site.
- **What you'll build**: We'll build a simple GitHub Pages site with a blog. We'll use [Jekyll](https://jekyllrb.com), a static site generator.
- **Prerequisites**: If you need to learn about branches, commits, and pull requests, take [Introduction to GitHub](https://github.com/skills/introduction-to-github) first.
- **How long**: This course takes less than one hour to complete.

In this course, you will:

1. Enable GitHub Pages
2. Configure your site
3. Customize your home page
4. Create a blog post
5. Merge your pull request

### How to start this course

<!-- For start course, run in JavaScript:
'https://github.com/new?' + new URLSearchParams({
  template_owner: 'skills',
  template_name: 'github-pages',
  owner: '@me',
  name: 'skills-github-pages',
  description: 'My clone repository',
  visibility: 'public',
}).toString()
-->

[![start-course](https://user-images.githubusercontent.com/1221423/235727646-4a590299-ffe5-480d-8cd5-8194ea184546.svg)](https://github.com/new?template_owner=skills&template_name=github-pages&owner=%40me&name=skills-github-pages&description=My+clone+repository&visibility=public)

1. Right-click **Start course** and open the link in a new tab.
2. In the new tab, most of the prompts will automatically fill in for you.
   - For owner, choose your personal account or an organization to host the repository.
   - We recommend creating a public repository, as private repositories will [use Actions minutes](https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions).
   - Scroll down and click the **Create repository** button at the bottom of the form.
3. After your new repository is created, wait about 20 seconds, then refresh the page. Follow the step-by-step instructions in the new repository's README.

<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/github-pages) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2023 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>
