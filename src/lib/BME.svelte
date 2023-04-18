<script>
  import socials from "$lib/assets/socials.json";
  let social = socials[0];

  const banner = "https://lh3.googleusercontent.com/drive-viewer/AAOQEOTMT4oFOfB9CFLO7QSPBjBqdrQvfkffNvnmYKAQNg8JfJModmpq2iGJHXx-Imh-Z6-lfvBNpXWvYn8L66fxHRYhrKFh=s1600";

  let width;

</script>

<p><img alt="banner" src={banner} width={width}>
</p>

<h1>
  Burn-and-mint tokenomics
</h1>

<p bind:clientWidth={width}>
  Since last year, I have been working at <a href="https://onocoy.com" target="_blank">onocoy</a>,
  a decentralized physical infrastructure (dePIN) project aiming to bring affordable
  high-precision positioning to the entire world. Like many dePIN projects, including
  the original <a href="https://helium.com" target="_blank">Helium</a>, we implement
  our tokenomics using burn-and-mint.
</p>
<p>
  In burn-and-mint, a token is "burned" <i>in nihilum</i> to pay for a service that a network provides; 
  a token is "minted" <i>ex nihilo</i> to pay for a service that is provided to the network. The mint
  pays for the supply of a service, and the demand pays for the burn. Burn-and-mint is useful because 
  it is a way to avoid raising fiat funds to bootstrap a network.
</p>
<p>
  There are so many questions that should be answered on the best way to design a burn-and-mint economy
  and I have set about answering some of them, with two posts appearing on my <a href={social.blog} target="_blank">blog</a>.
  Questions that are important to the industry include:
</p>
<ul>
  <li>What is the net present value of a burn-and-mint economy?
    (see answer <a href="{social.blog}/valuing-burn-and-mint" target="_blank">here</a>)</li> 
  <li>How much should contributers be rewarded?
    (see answer <a href="{social.blog}/adequate-burn-and-mint-rewards" target="_blank">here</a>)</li>
  <li>How does uncertainty around an economy's value affect volatility of the token price?</li>
  <li>How can an economy be designed to soften the impact of shocks such as dumping or crypto market volatility?</li>
  <li>what is the interplay between staking and burn-and-mint?</li>
  <li>In a world of infinitely many Nash equilibria, how can an economy be designed to ensure 
    an acceptable outcome for all participants?</li>  
</ul>
<p>
  I wrote the above in the order that I plan to answer these questions. To work on this, I have partnered
  up with my fellow onos and some experts in the fields of tokenomics and economic game theory. Note that
  most of the questions above are not specifically limited to burn-and-mint economies, so this research might
  answer questions surrounding other types of tokenomic models and even shed light on the mathematics and
  gamesmanship behind traditional financial systems.
</p>
<p>
  Henceforth this page will act as a central place where I will present my research into tokenomics. My hope
  is that we as a field can break into the mainstream, with representation at conferences like 
  Economics and Computation and Financial Cryptography. 
</p>

