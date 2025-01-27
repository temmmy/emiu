<script>
    import img from "$lib/images/flowers.svg";
    let isToggled = true;
</script>

<div class="fixed-header">
    <img src={img} alt="Flower Icon" class="flower-icon" />
    <h1>Đỗ Thuỳ Linh</h1>
</div>
<div class="container">
    <div class={isToggled ? "image-section" : "image-section-5"}></div>
    <div class="text-section">
        <h2>
            {isToggled
                ? "Gửi đến em những lời chúc tốt đẹp nhất. Anh đã tìm hoa khắp nơi nhưng không thể nào kiếm được bó hoa nào thật đặc biệt dành cho em."
                : "Chửi anh ít thôi =)))"}
        </h2>
    </div>
</div>
<div class="container">
    <div class="text-section-2">
        <h2 style="color: #3e3e4f">
            {isToggled
                ? "Vì thế, anh đã quyết định tự làm một món quà đặc biệt cho em – một trang ngập tràn những bông hoa mà em yêu thích."
                : "Đậy Sớm vào =)))"}
        </h2>
    </div>
    <div class={isToggled ? "image-section-2" : "image-section-6"}></div>
</div>
<div class="container">
    <div class={isToggled ? "image-section-3" : "image-section-7"}></div>
    <div class="text-section-3">
        <h2 style="color: #4f373c">
            {isToggled
                ? "Cảm ơn em vì đã cùng anh đi đến tận cùng thế giới. Chúc em sinh nhật hạnh phúc, đầy yêu thương và ngọt ngào như chính em vậy."
                : "Bớt Mood Swing đi =)))"}
        </h2>
    </div>
</div>
<div class="container">
    <div class="text-section-4">
        <h2 style="color: #e1dfd3">
            {isToggled
                ? "Anh mong rằng chúng ta sẽ mãi bên nhau, cùng nhau viết tiếp những chương mới thật đẹp cho câu chuyện của mình."
                : "??? =)))"}
        </h2>
        <div class="button-section">
            <button on:click={() => (isToggled = false)} class="button"
                >No</button
            >
            <button on:click={() => (isToggled = true)} class="button"
                >Yes</button
            >
        </div>
    </div>
    <div class={isToggled ? "image-section-4" : "image-section-8"}></div>
</div>

<style>
    :global(body) {
        margin: 0;
        font-family: Arial, sans-serif;
    }

    @font-face {
        font-family: "MainD";
        font-style: normal;
        font-display: swap;
        font-weight: 700;
        src: url("$lib/fonts/DFVN ED Lavonia.otf") format("opentype");
    }

    @font-face {
        font-family: "MainA";
        font-style: normal;
        font-display: swap;
        font-weight: 700;
        src: url("$lib/fonts/BeautiqueDisplay-Regular.otf") format("opentype");
    }

    @font-face {
        font-family: "MainB";
        font-style: normal;
        font-display: swap;
        font-weight: 700;
        src: url("$lib/fonts/BeautiqueDisplay-Bold.otf") format("opentype");
    }

    .fixed-header {
        position: fixed;
        top: 2%;
        left: 50%;
        transform: translateX(-50%);
        display: flex;
        flex-direction: column;
        align-items: center;
        z-index: 10; /* Ensure it's above other content */
        padding: 10px;
        border-radius: 10px; /* Optional styling */
    }

    .container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        height: 100vh;
    }

    .image-section {
        background-image: url("/src/lib/images/hero.jpg");
        background-size: cover;
        background-position: center;
    }

    .image-section-2 {
        background-image: url("/src/lib/images/love.jpg");
        background-size: cover;
        background-position: center;
    }

    .image-section-3 {
        background-image: url("/src/lib/images/you.JPG");
        background-size: cover;
        background-position: center;
    }
    .image-section-4 {
        background-image: url("/src/lib/images/beach.jpg");
        background-size: cover;
        background-position: center;
    }

    .image-section-5 {
        background-image: url("/src/lib/images/haha.JPG");
        background-size: cover;
        background-position: center;
    }

    .image-section-6 {
        background-image: url("/src/lib/images/haha3.JPG");
        background-size: cover;
        background-position: center;
    }

    .image-section-7 {
        background-image: url("/src/lib/images/haha4.JPG");
        background-size: cover;
        background-position: center;
    }

    .image-section-8 {
        background-image: url("/src/lib/images/haha2.JPG");
        background-size: cover;
        background-position: center;
    }

    .text-section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 5rem;
        background-image: url("/src/lib/images/blue.jpg");
        background-position: center;
        color: white;
    }

    .text-section-2 {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 5rem;
        background-image: url("/src/lib/images/flowers.jpg");
        background-position: center;
        color: white;
    }

    .text-section-3 {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 5rem;
        background-image: url("/src/lib/images/flowers5.jpg");
        background-size: cover;
        background-position: center;
        color: white;
    }

    .text-section-4 {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 5rem;
        background-image: url("/src/lib/images/purple.jpg");
        background-size: cover;
        background-position: center;
        color: white;
    }

    .flower-icon {
        width: 10vh; /* Adjust the size */
        height: 10vh;
        margin-bottom: 0vh; /* Space between icon and text */
        color: #d3c6b9;
    }
    .button {
        background-color: #d3c6b9;
        color: white;
        padding: 10px 20px;
        border: none;
        border-radius: 50px;
        font-family: "MainA";
        font-size: 3vh;
        cursor: pointer;
        margin: 10px;
    }

    .button:hover {
        background-color: #b9a38c;
    }
    h1 {
        font-family: "MainD";
        font-size: 8vh;
        margin: 0;
        color: #d3c6b9;
    }

    h2 {
        font-family: "MainB";
        font-size: 5.2vh;
        margin: 0;
        color: #d3c6b9;
        /* text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5); */
        text-shadow: 2px 3px 5px rgba(0, 0, 0, 0.3);
    }
</style>
