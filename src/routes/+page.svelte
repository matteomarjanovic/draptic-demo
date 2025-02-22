<script>
    let email = "";

    async function handleSubmit() {
        // TODO: Implement email signup logic
        console.log("Email submitted:", email);
    }
</script>

<svelte:head>
    <script
        type="module"
        src="https://gradio.s3-us-west-2.amazonaws.com/5.0.1/gradio.js"
    ></script>
    <script
        defer
        src="https://mm-umami.netlify.app/script.js"
        data-website-id="b80ba154-c32c-47aa-b133-6ab977537dbf"
    ></script>
</svelte:head>

<div class="min-h-screen bg-base-100">
    <!-- Hero Section -->
    <div class="hero min-h-screen bg-base-200">
        <div class="hero-content text-center">
            <div class="max-w-md">
                <h1 class="text-5xl font-bold">Draptic</h1>
                <p class="py-6">
                    Transform your garment images into professional technical
                    flat sketches instantly with AI-powered technology.
                </p>
                <div class="flex justify-center items-center gap-4">
                    <a href="#demo" class="btn btn-primary">Try Demo</a>
                    <a href="#signup" class="btn btn-secondary">Sign Up</a>
                </div>
            </div>
        </div>
    </div>

    <!-- Demo Section -->
    <div id="demo" class="container mx-auto py-16 px-4">
        <h2 class="text-3xl font-bold text-center mb-8">See It in Action</h2>
        <div class="w-full max-w-4xl mx-auto bg-base-300 rounded-box">
            <!-- <iframe
                title="Draptic Demo"
                src="https://matteomarjanovic-draptic-demo.hf.space"
                class="w-full h-full rounded-box"
            ></iframe> -->
            <gradio-app
                src="https://matteomarjanovic-draptic-demo.hf.space/?__theme=light"
                theme_mode="light"
            ></gradio-app>
        </div>
    </div>

    <!-- Sign Up Section -->
    <div id="signup" class="bg-base-200 py-16">
        <div class="container mx-auto px-4">
            <div class="max-w-md mx-auto text-center">
                <h2 class="text-3xl font-bold mb-4">Get Early Access</h2>
                <p class="mb-8">
                    Sign up to be notified when the full version launches!
                </p>
                <form
                    class="flex flex-col gap-4"
                    name="mailing-list"
                    data-netlify="true"
                >
                    <input
                        type="hidden"
                        name="form-name"
                        value="mailing-list"
                    />
                    <input
                        type="email"
                        bind:value={email}
                        name="email"
                        placeholder="Enter your email"
                        class="input input-bordered w-full"
                        required
                    />
                    <button type="submit" class="btn btn-primary"
                        >Sign Up</button
                    >
                </form>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="footer footer-center p-10 bg-base-300 text-base-content">
        <div>
            <p>© 2025 - All rights reserved by Draptic</p>
        </div>
    </footer>
</div>
