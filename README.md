<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Testimony Connect</title>
<style>
body {
  font-family: Arial, sans-serif;
  background: #f5f2fa;
  margin: 0;
  color: #302344;
}
header {
  background: #49316b;
  color: white;
  text-align: center;
  padding: 35px 15px;
}
main {
  max-width: 650px;
  margin: 25px auto;
  padding: 15px;
}
.card {
  background: white;
  padding: 20px;
  border-radius: 12px;
  margin-bottom: 18px;
}
input, textarea, button {
  width: 100%;
  padding: 12px;
  margin: 8px 0;
  box-sizing: border-box;
}
button {
  background: #49316b;
  color: white;
  border: 0;
  border-radius: 7px;
  cursor: pointer;
}
footer {
  text-align: center;
  padding: 20px;
}
</style>
</head>
<body>

<header>
  <h1>Testimony Connect</h1>
  <p>Your story can give someone hope.</p>
</header>

<main>
  <section class="card">
    <h2>Share Your Testimony</h2>
    <form id="storyForm">
      <input id="name" placeholder="Your name (or Anonymous)" required>
      <textarea id="story" placeholder="Share your testimony..." required></textarea>
      <button type="submit">Share My Story</button>
    </form>
    <p id="message"></p>
  </section>

  <section class="card">
    <h2>Inspiring Testimonies</h2>
    <div id="stories">
      <p>Be the first to share a story of hope!</p>
    </div>
  </section>

  <section class="card">
    <h2>Today's Bible Verse</h2>
    <p>"I can do all things through Christ which strengtheneth me."</p>
    <b>Philippians 4:13</b>
  </section>
</main>

<footer>
  <p>Testimony Connect © 2026</p>
  <p>Sharing hope, faith and encouragement.</p>
</footer>

<script>
document.getElementById("storyForm").onsubmit = function(e) {
  e.preventDefault();

  const name = document.getElementById("name").value;
  const story = document.getElementById("story").value;

  const card = document.createElement("div");
  const heading = document.createElement("h3");
  const paragraph = document.createElement("p");

  heading.textContent = name;
  paragraph.textContent = story;
  card.append(heading, paragraph);

  document.getElementById("stories").prepend(card);
  document.getElementById("message").textContent =
    "Thank you for sharing your story!";

  this.reset();
};
</script>

</body>
</html>
