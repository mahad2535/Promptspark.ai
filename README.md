<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="PromptSpark.ai - Free AI prompts generator for social media and marketing. Instantly generate Instagram captions, TikTok scripts, LinkedIn posts, and email/ad copy.">
  <title>PromptSpark.ai - AI Prompt Generator for Social Media & Marketing</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f0f4f8;
      color: #333;
      margin: 0;
      padding: 0;
      text-align: center;
    }
    header {
      background: #5c6bc0;
      color: white;
      padding: 20px 0;
      margin-bottom: 20px;
    }
    h1 {
      margin: 0;
      font-size: 2em;
    }
    select, button {
      padding: 10px;
      font-size: 1em;
      margin: 10px 0;
    }
    #promptDisplay {
      margin: 20px auto;
      padding: 20px;
      width: 90%;
      max-width: 600px;
      background: white;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      min-height: 80px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
    }
    footer {
      margin-top: 40px;
      padding: 10px;
      font-size: 0.9em;
      color: #555;
    }
  </style>
</head>
<body>

<header>
  <h1>PromptSpark.ai</h1>
  <p>Generate free AI prompts for social media & marketing instantly!</p>
</header>

<main>
  <label for="categorySelect">Select a category:</label>
  <br>
  <select id="categorySelect">
    <option value="instagram">Instagram Captions & Reels</option>
    <option value="tiktok">TikTok Scripts & Short Videos</option>
    <option value="linkedin">LinkedIn Posts & Engagement</option>
    <option value="email">Email & Ad Copy</option>
  </select>
  <br>
  <button onclick="generatePrompt()">Generate Prompt</button>
  <button onclick="copyPrompt()">Copy Prompt</button>

  <div id="promptDisplay">Your AI prompt will appear here!</div>
</main>

<footer>
  &copy; 2025 PromptSpark.ai | Free AI Prompt Generator for Social Media & Marketing
</footer>

<script>
const prompts = {
  instagram: [
    "Write a funny caption about productivity using AI",
    "Generate 5 viral Instagram captions for a tech startup",
    "Create a motivational caption for personal growth niche",
    "Write a short reel script about AI tools for small businesses",
    "Make an Instagram carousel idea for 'Top 5 AI hacks'",
    "Create a witty caption for a travel photo",
    "Generate 3 Instagram captions for a fitness brand",
    "Write a catchy caption for an eco-friendly product",
    "Create a reel idea for a cooking tutorial",
    "Write 5 hashtags for a marketing post",
    "Create a caption promoting a webinar",
    "Write an engaging caption for a product launch",
    "Generate captions for a motivational quote series",
    "Create a humorous caption about AI tools",
    "Write a carousel caption about top 10 marketing tips",
    "Generate a caption for a behind-the-scenes photo",
    "Write a caption for a giveaway post",
    "Create an Instagram caption about AI art",
    "Generate a caption for a tech review post",
    "Write a short story-style caption for Instagram"
  ],
  tiktok: [
    "Generate a 15-second script for a TikTok on AI productivity tips",
    "Write a humorous TikTok about remote working",
    "Create a step-by-step tutorial script for Canva AI",
    "Generate a challenge idea for TikTok about AI art",
    "Write a trending TikTok voiceover script about marketing hacks",
    "Create a hook for a TikTok about social media growth",
    "Generate a script for a TikTok tutorial video",
    "Write a funny TikTok scenario about AI tools",
    "Create a step-by-step TikTok script for content creation",
    "Generate a 30-second TikTok pitch for a small business",
    "Write a trending TikTok script for a digital marketing tip",
    "Create a viral TikTok idea for productivity hacks",
    "Generate a creative script for a cooking TikTok",
    "Write a TikTok script promoting an online course",
    "Create a short TikTok dialogue for AI tools",
    "Generate a funny TikTok about home office life",
    "Write a TikTok hook for social media marketing",
    "Create a script for a mini TikTok storytelling video",
    "Generate a TikTok idea for promoting AI art",
    "Write a viral TikTok about digital tools"
  ],
  linkedin: [
    "Write a professional LinkedIn post on AI in digital marketing",
    "Generate a LinkedIn article intro about productivity tools",
    "Draft a networking message for LinkedIn using AI",
    "Create 5 engaging post ideas for a SaaS startup",
    "Write a post highlighting a recent marketing trend",
    "Generate a LinkedIn post about AI for entrepreneurs",
    "Write a professional LinkedIn summary for a marketer",
    "Create a post about remote work productivity tips",
    "Draft a post celebrating a business milestone",
    "Generate a LinkedIn article idea about AI tools",
    "Write a post engaging your network about a new project",
    "Create a professional post about marketing automation",
    "Generate tips for LinkedIn engagement using AI",
    "Write a post about emerging AI trends in business",
    "Draft a LinkedIn post promoting a webinar",
    "Generate a post showcasing your brand story",
    "Write a LinkedIn post about leadership and AI",
    "Create an informative post on AI marketing strategies",
    "Generate 3 post ideas for personal branding",
    "Write a LinkedIn post summarizing a recent case study"
  ],
  email: [
    "Generate a subject line for a promotional email about AI tools",
    "Write ad copy for Facebook targeting small business owners",
    "Create a Google Ads headline for a digital marketing service",
    "Generate a newsletter intro about AI in social media marketing",
    "Write 3 email variations for a product launch campaign",
    "Create a subject line for a new course announcement",
    "Write ad copy for Instagram promoting AI tools",
    "Generate an email introducing a new product feature",
    "Create a CTA for email marketing campaigns",
    "Write a Facebook ad targeting digital marketers",
    "Generate email ideas for webinar promotion",
    "Create 3 variations of newsletter headlines",
    "Write a Google Ads description for a SaaS tool",
    "Generate an email promoting a free AI resource",
    "Write ad copy for LinkedIn targeting startups",
    "Create a newsletter paragraph for engagement tips",
    "Generate a product launch email series",
    "Write Facebook ad copy for AI-powered software",
    "Create catchy subject lines for email campaigns",
    "Generate 3 ad variations for a social media campaign"
  ]
};

function generatePrompt() {
  const category = document.getElementById("categorySelect").value;
  const randomIndex = Math.floor(Math.random() * prompts[category].length);
  document.getElementById("promptDisplay").innerText = prompts[category][randomIndex];
}

function copyPrompt() {
  const promptText = document.getElementById("promptDisplay").innerText;
  navigator.clipboard.writeText(promptText).then(() => {
    alert("Prompt copied to clipboard!");
  });
}
</script>

</body>
</html>
