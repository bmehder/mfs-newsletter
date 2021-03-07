<svelte:options tag="mfs-newsletter" />

<script>
  export let background = "#307ad5";
  export let color = "white";
  export let buttonColor = "#fdc735";
  export let src = "";
</script>

<article style="background:{background};color:{color};">
  {#if src}
    <img {src} alt="MyFunScience Newsletter Signup" />
  {/if}
  <h3><span>Get $50 Off</span> Your First Class</h3>
  <p>Subscribe to the mailing list, and get a $50 coupon!</p>

  <form
    id="mc-embedded-subscribe-form"
    class="validate"
    action="https://myfunscience.us14.list-manage.com/subscribe/post?u=30c96ba77f289432950d9d899&amp;id=2a42246b40"
    method="post"
    name="mc-embedded-subscribe-form"
    novalidate=""
    target="_blank"
  >
    <input
      name="EMAIL"
      type="email"
      placeholder="Enter email address..."
      required
    />
    <div style="position: absolute; left: -5000px;" aria-hidden="true">
      <input
        tabindex="-1"
        name="b_30c96ba77f289432950d9d899_2a42246b40"
        type="text"
        value=""
      />
    </div>
    <input style="background:{buttonColor}" type="submit" value="Subscribe" />
  </form>
</article>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600&display=swap");
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    font-family: "Open Sans", sans-serif;
  }
  article {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1em;
    max-width: 600px;
    padding: 2em 2em 3em;
    text-align: center;
    border-radius: 16px;
  }
  img {
    width: 50%;
    height: auto;
    margin: 1em;
    border-radius: 50%;
    transition: 0.4s ease-in-out transform, 0.4s ease-in-out box-shadow;
    animation: hover 8s infinite ease-in-out;
    animation-delay: 5s;
  }
  @keyframes hover {
    0% {
      transform: rotateX(0deg) rotateZ(0deg);
      box-shadow: none;
    }
    20% {
      transform: rotateX(52deg) rotateZ(42deg);
      transform-style: preserve-3d;
      box-shadow: 1px 1px 0 1px #f9f9fb, -1px 0 28px 0 rgba(34, 33, 81, 0.01),
        28px 28px 28px 0 rgba(34, 33, 81, 0.25);
    }
    50% {
      transform: rotateX(-52deg) rotateY(-32deg) rotateZ(-42deg);
      transform-style: preserve-3d;
      box-shadow: 1px 1px 0 1px #f9f9fb, -1px 0 28px 0 rgba(34, 33, 81, 0.01),
        28px 28px 28px 0 rgba(34, 33, 81, 0.25);
    }
    70% {
      transform: rotateX(0deg) rotateZ(0deg);
      box-shadow: none;
    }
  }
  h3 {
    margin-top: 0.5em;
    font-size: 1.5em;
    line-height: 1.4em;
    font-weight: 300;
    text-transform: uppercase;
    letter-spacing: 0.24em;
  }
  span {
    font-weight: bold;
  }
  p {
    margin: 1em 0;
    font-size: 1.1em;
    line-height: 1.5;
  }
  form {
    width: 80%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  input {
    width: 100%;
    margin-bottom: 0.5em;
    padding: 1em;
    text-align: center;
    font-size: 1em;
    outline: none;
    border: none;
    border-radius: 4px;
    transition: 100ms;
  }
  input[type="submit"] {
    color: #333;
    font-weight: bold;
    text-transform: uppercase;
  }
  @media screen and (max-width: 400px) {
    img {
      width: 80%;
    }
  }
</style>
