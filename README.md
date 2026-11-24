<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Display Videos in an iframe</title>
    <style>
      * { box-sizing: border-box; margin: 0; padding: 0; }

      body {
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        gap: 28px;
        padding: 40px 20px;
        font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
        color: #fff;
        background:
          radial-gradient(circle at 15% 20%, rgba(255, 79, 163, 0.35), transparent 45%),
          radial-gradient(circle at 85% 80%, rgba(58, 123, 255, 0.35), transparent 45%),
          #0b0f1f;
      }

      h1 {
        font-size: clamp(1.8rem, 6vw, 3rem);
        font-weight: 800;
        letter-spacing: -0.02em;
        text-align: center;
        background: linear-gradient(90deg, #ff7eb3, #7aa7ff);
        -webkit-background-clip: text;
        background-clip: text;
        color: transparent;
      }

      /* Glass frame around the video */
      .frame {
        width: 100%;
        max-width: 760px;
        padding: 14px;
        border-radius: 24px;
        background: linear-gradient(135deg, rgba(255, 255, 255, 0.2), rgba(255, 255, 255, 0.05));
        border: 1px solid rgba(255, 255, 255, 0.25);
        box-shadow:
          inset 0 1px 0 rgba(255, 255, 255, 0.5),
          0 25px 60px rgba(0, 0, 0, 0.5);
        -webkit-backdrop-filter: blur(20px);
        backdrop-filter: blur(20px);
      }

      iframe {
        display: block;
        width: 100%;
        height: auto;
        aspect-ratio: 16 / 9;
        border: 0;
        border-radius: 14px;
        background: #000;
      }
    </style>
  </head>
  <body>
    <h1>iframe Video Display</h1>
    <div class="frame">
      <iframe
        width="560"
        height="315"
        src="https://www.youtube.com/embed/I0_951_MPE0"
        allow="accelerometer autoplay clipboard-write encrypted-media gyroscope web-share"
        referrerpolicy="strict-origin-when-cross-origin"
        allowfullscreen
      ></iframe>
    </div>
  </body>
</html>