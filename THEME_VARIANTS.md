# Cinematch Theme Variants

This document provides three complete visual styling variants for the Cinematch movie recommendation website. Each theme features a unique full-page background gradient and styled section containers using modern CSS techniques.

## Theme Overview

### 🌅 Theme 1: Sunset Cinema
- **Background**: Warm orange to deep blue diagonal gradient
- **Style**: Glass morphism with enhanced blur effects
- **Mood**: Warm, cinematic, golden hour vibes

### 🌙 Theme 2: Midnight Elegance
- **Background**: Violet to pink diagonal gradient
- **Style**: Gradient overlay containers with premium feel
- **Mood**: Sophisticated, modern, luxurious

### ❄️ Theme 3: Arctic Cool
- **Background**: Teal to gray diagonal gradient
- **Style**: Frosted glass with maximum blur
- **Mood**: Clean, cool, minimalist

---

## 🌅 Theme 1: Sunset Cinema

### Files to Create:

#### `theme1-sunset-index.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Cinematch - Your Movie Recommendation Platform</title>
    <!-- Tailwind CSS via CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body { font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif; }
        .content-wrapper { padding-top: 4rem; }
        .scrollbar-hide { -ms-overflow-style: none; scrollbar-width: none; }
        .scrollbar-hide::-webkit-scrollbar { display: none; }
    </style>
</head>
<body class="bg-gradient-to-br from-orange-400 via-red-500 to-blue-900 min-h-screen text-white">
    <!-- Header placeholder -->
    <div id="header-placeholder"></div>

    <!-- Main content -->
    <div class="content-wrapper">
        <main class="container mx-auto px-4 sm:px-6 lg:px-8 py-8">
            <div class="mb-8">
                <h2 class="text-4xl font-bold text-white tracking-tight drop-shadow-lg bg-gradient-to-r from-orange-200 to-yellow-200 bg-clip-text text-transparent">Welcome to Cinematch</h2>
                <p class="text-orange-100 mt-3 text-lg drop-shadow-md">Your personalized movie and TV show recommendation platform.</p>
            </div>

            <!-- Trending Now -->
            <section class="bg-white/20 backdrop-blur-xl rounded-2xl shadow-2xl border border-white/30 p-8 mb-8 hover:bg-white/25 transition-all duration-300">
                <h3 class="text-2xl font-bold text-white mb-4 drop-shadow-md bg-gradient-to-r from-orange-300 to-yellow-300 bg-clip-text text-transparent">Trending Now</h3>
                <div class="overflow-x-auto overflow-y-hidden snap-x snap-mandatory scroll-smooth touch-pan-x cursor-grab" data-hscroll>
                    <div id="trending-row" class="flex flex-nowrap gap-x-6 pb-3 min-w-max"></div>
                </div>
            </section>

            <!-- Top Rated with toggle -->
            <section class="bg-white/20 backdrop-blur-xl rounded-2xl shadow-2xl border border-white/30 p-8 mb-8 hover:bg-white/25 transition-all duration-300">
                <div class="flex items-center justify-between mb-4">
                    <h3 class="text-2xl font-bold text-white drop-shadow-md bg-gradient-to-r from-orange-300 to-yellow-300 bg-clip-text text-transparent">Top Rated</h3>
                    <div class="inline-flex rounded-xl border border-orange-400/50 overflow-hidden bg-white/20 backdrop-blur-md" role="group">
                        <button id="btn-top-movies" type="button" class="px-4 py-2 text-sm font-semibold bg-gradient-to-r from-orange-500 to-red-500 text-white transition-all duration-200">Movies</button>
                        <button id="btn-top-tv" type="button" class="px-4 py-2 text-sm font-semibold bg-transparent text-white hover:bg-white/20 transition-all duration-200">TV Shows</button>
                    </div>
                </div>
                <div class="overflow-x-auto overflow-y-hidden snap-x snap-mandatory scroll-smooth touch-pan-x cursor-grab" data-hscroll>
                    <div id="top-rated-row" class="flex flex-nowrap gap-x-6 pb-3 min-w-max"></div>
                </div>
            </section>

            <!-- Now Playing -->
            <section class="bg-white/20 backdrop-blur-xl rounded-2xl shadow-2xl border border-white/30 p-8 hover:bg-white/25 transition-all duration-300">
                <h3 class="text-2xl font-bold text-white mb-4 drop-shadow-md bg-gradient-to-r from-orange-300 to-yellow-300 bg-clip-text text-transparent">Now Playing</h3>
                <div class="overflow-x-auto overflow-y-hidden snap-x snap-mandatory scroll-smooth touch-pan-x cursor-grab" data-hscroll>
                    <div id="now-playing-row" class="flex flex-nowrap gap-x-6 pb-3 min-w-max"></div>
                </div>
            </section>
        </main>
    </div>

    <!-- JavaScript remains the same as original -->
    <script>
        // [Include all the original JavaScript functionality here]
        // Load header, scroll functionality, API calls, etc.
    </script>
</body>
</html>
```

#### `theme1-sunset-header.html`
```html
<header class="fixed top-0 left-0 right-0 z-40 bg-black/40 backdrop-blur-xl border-b border-white/20 shadow-2xl">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-16">
            <!-- Logo -->
            <div class="flex-shrink-0">
                <h1 class="text-2xl font-bold bg-gradient-to-r from-orange-400 to-yellow-400 bg-clip-text text-transparent cursor-pointer">Cinematch</h1>
            </div>

            <!-- Desktop Navigation -->
            <nav class="hidden md:flex items-center space-x-8">
                <!-- Search Bar -->
                <div class="relative bg-white/20 backdrop-blur-md border border-orange-400/50 rounded-xl">
                    <input type="text" placeholder="Search movies, TV shows..." class="bg-transparent text-white border-none outline-none w-full px-4 py-2 text-sm rounded-xl placeholder-orange-200" />
                </div>

                <!-- User Dropdown -->
                <div class="user-dropdown">
                    <button class="user-button flex items-center space-x-2 text-white px-3 py-2 rounded-lg">
                        <div class="w-8 h-8 bg-gradient-to-br from-orange-500 to-red-600 rounded-full flex items-center justify-center text-sm font-semibold">U</div>
                        <span class="hidden lg:block text-sm font-medium">User</span>
                    </button>
                    <!-- Dropdown menu with warm theme styling -->
                </div>
            </nav>
        </div>
    </div>
</header>
```

---

## 🌙 Theme 2: Midnight Elegance

### Files to Create:

#### `theme2-midnight-index.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Cinematch - Your Movie Recommendation Platform</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body { font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif; }
        .content-wrapper { padding-top: 4rem; }
        .scrollbar-hide { -ms-overflow-style: none; scrollbar-width: none; }
        .scrollbar-hide::-webkit-scrollbar { display: none; }
    </style>
</head>
<body class="bg-gradient-to-br from-violet-900 via-purple-800 to-pink-700 min-h-screen text-white">
    <!-- Header placeholder -->
    <div id="header-placeholder"></div>

    <!-- Main content -->
    <div class="content-wrapper">
        <main class="container mx-auto px-4 sm:px-6 lg:px-8 py-8">
            <div class="mb-8">
                <h2 class="text-4xl font-bold text-white tracking-tight drop-shadow-lg bg-gradient-to-r from-pink-200 to-violet-200 bg-clip-text text-transparent">Welcome to Cinematch</h2>
                <p class="text-pink-100 mt-3 text-lg drop-shadow-md">Your personalized movie and TV show recommendation platform.</p>
            </div>

            <!-- Trending Now -->
            <section class="bg-gradient-to-r from-purple-900/80 to-pink-900/80 backdrop-blur-lg rounded-2xl shadow-2xl border border-pink-500/30 p-8 mb-8 hover:from-purple-900/90 hover:to-pink-900/90 transition-all duration-300">
                <h3 class="text-2xl font-bold text-white mb-4 drop-shadow-md bg-gradient-to-r from-pink-300 to-violet-300 bg-clip-text text-transparent">Trending Now</h3>
                <div class="overflow-x-auto overflow-y-hidden snap-x snap-mandatory scroll-smooth touch-pan-x cursor-grab" data-hscroll>
                    <div id="trending-row" class="flex flex-nowrap gap-x-6 pb-3 min-w-max"></div>
                </div>
            </section>

            <!-- Top Rated with toggle -->
            <section class="bg-gradient-to-r from-purple-900/80 to-pink-900/80 backdrop-blur-lg rounded-2xl shadow-2xl border border-pink-500/30 p-8 mb-8 hover:from-purple-900/90 hover:to-pink-900/90 transition-all duration-300">
                <div class="flex items-center justify-between mb-4">
                    <h3 class="text-2xl font-bold text-white drop-shadow-md bg-gradient-to-r from-pink-300 to-violet-300 bg-clip-text text-transparent">Top Rated</h3>
                    <div class="inline-flex rounded-xl border border-pink-400/50 overflow-hidden bg-gradient-to-r from-purple-800/60 to-pink-800/60 backdrop-blur-md" role="group">
                        <button id="btn-top-movies" type="button" class="px-4 py-2 text-sm font-semibold bg-gradient-to-r from-pink-500 to-violet-500 text-white transition-all duration-200">Movies</button>
                        <button id="btn-top-tv" type="button" class="px-4 py-2 text-sm font-semibold bg-transparent text-white hover:bg-gradient-to-r hover:from-pink-600/30 hover:to-violet-600/30 transition-all duration-200">TV Shows</button>
                    </div>
                </div>
                <div class="overflow-x-auto overflow-y-hidden snap-x snap-mandatory scroll-smooth touch-pan-x cursor-grab" data-hscroll>
                    <div id="top-rated-row" class="flex flex-nowrap gap-x-6 pb-3 min-w-max"></div>
                </div>
            </section>

            <!-- Now Playing -->
            <section class="bg-gradient-to-r from-purple-900/80 to-pink-900/80 backdrop-blur-lg rounded-2xl shadow-2xl border border-pink-500/30 p-8 hover:from-purple-900/90 hover:to-pink-900/90 transition-all duration-300">
                <h3 class="text-2xl font-bold text-white mb-4 drop-shadow-md bg-gradient-to-r from-pink-300 to-violet-300 bg-clip-text text-transparent">Now Playing</h3>
                <div class="overflow-x-auto overflow-y-hidden snap-x snap-mandatory scroll-smooth touch-pan-x cursor-grab" data-hscroll>
                    <div id="now-playing-row" class="flex flex-nowrap gap-x-6 pb-3 min-w-max"></div>
                </div>
            </section>
        </main>
    </div>

    <!-- JavaScript remains the same as original -->
    <script>
        // [Include all the original JavaScript functionality here]
    </script>
</body>
</html>
```

#### `theme2-midnight-header.html`
```html
<header class="fixed top-0 left-0 right-0 z-40 bg-gradient-to-r from-purple-900/60 to-pink-900/60 backdrop-blur-xl border-b border-pink-500/30 shadow-2xl">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-16">
            <!-- Logo -->
            <div class="flex-shrink-0">
                <h1 class="text-2xl font-bold bg-gradient-to-r from-pink-400 to-violet-400 bg-clip-text text-transparent cursor-pointer">Cinematch</h1>
            </div>

            <!-- Desktop Navigation -->
            <nav class="hidden md:flex items-center space-x-8">
                <!-- Search Bar -->
                <div class="relative bg-gradient-to-r from-purple-800/30 to-pink-800/30 backdrop-blur-md border border-pink-400/50 rounded-xl">
                    <input type="text" placeholder="Search movies, TV shows..." class="bg-transparent text-white border-none outline-none w-full px-4 py-2 text-sm rounded-xl placeholder-pink-200" />
                </div>

                <!-- User Dropdown -->
                <div class="user-dropdown">
                    <button class="user-button flex items-center space-x-2 text-white px-3 py-2 rounded-lg">
                        <div class="w-8 h-8 bg-gradient-to-br from-pink-500 to-violet-600 rounded-full flex items-center justify-center text-sm font-semibold">U</div>
                        <span class="hidden lg:block text-sm font-medium">User</span>
                    </button>
                    <!-- Dropdown menu with midnight theme styling -->
                </div>
            </nav>
        </div>
    </div>
</header>
```

---

## ❄️ Theme 3: Arctic Cool

### Files to Create:

#### `theme3-arctic-index.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Cinematch - Your Movie Recommendation Platform</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body { font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif; }
        .content-wrapper { padding-top: 4rem; }
        .scrollbar-hide { -ms-overflow-style: none; scrollbar-width: none; }
        .scrollbar-hide::-webkit-scrollbar { display: none; }
    </style>
</head>
<body class="bg-gradient-to-br from-teal-600 via-cyan-500 to-gray-600 min-h-screen text-white">
    <!-- Header placeholder -->
    <div id="header-placeholder"></div>

    <!-- Main content -->
    <div class="content-wrapper">
        <main class="container mx-auto px-4 sm:px-6 lg:px-8 py-8">
            <div class="mb-8">
                <h2 class="text-4xl font-bold text-white tracking-tight drop-shadow-lg bg-gradient-to-r from-cyan-200 to-teal-200 bg-clip-text text-transparent">Welcome to Cinematch</h2>
                <p class="text-cyan-100 mt-3 text-lg drop-shadow-md">Your personalized movie and TV show recommendation platform.</p>
            </div>

            <!-- Trending Now -->
            <section class="bg-white/10 backdrop-blur-2xl rounded-3xl shadow-2xl border border-white/20 p-8 mb-8 hover:bg-white/15 transition-all duration-300">
                <h3 class="text-2xl font-bold text-white mb-4 drop-shadow-md bg-gradient-to-r from-cyan-300 to-teal-300 bg-clip-text text-transparent">Trending Now</h3>
                <div class="overflow-x-auto overflow-y-hidden snap-x snap-mandatory scroll-smooth touch-pan-x cursor-grab" data-hscroll>
                    <div id="trending-row" class="flex flex-nowrap gap-x-6 pb-3 min-w-max"></div>
                </div>
            </section>

            <!-- Top Rated with toggle -->
            <section class="bg-white/10 backdrop-blur-2xl rounded-3xl shadow-2xl border border-white/20 p-8 mb-8 hover:bg-white/15 transition-all duration-300">
                <div class="flex items-center justify-between mb-4">
                    <h3 class="text-2xl font-bold text-white drop-shadow-md bg-gradient-to-r from-cyan-300 to-teal-300 bg-clip-text text-transparent">Top Rated</h3>
                    <div class="inline-flex rounded-2xl border border-cyan-400/50 overflow-hidden bg-white/10 backdrop-blur-xl" role="group">
                        <button id="btn-top-movies" type="button" class="px-4 py-2 text-sm font-semibold bg-gradient-to-r from-cyan-500 to-teal-500 text-white transition-all duration-200">Movies</button>
                        <button id="btn-top-tv" type="button" class="px-4 py-2 text-sm font-semibold bg-transparent text-white hover:bg-white/20 transition-all duration-200">TV Shows</button>
                    </div>
                </div>
                <div class="overflow-x-auto overflow-y-hidden snap-x snap-mandatory scroll-smooth touch-pan-x cursor-grab" data-hscroll>
                    <div id="top-rated-row" class="flex flex-nowrap gap-x-6 pb-3 min-w-max"></div>
                </div>
            </section>

            <!-- Now Playing -->
            <section class="bg-white/10 backdrop-blur-2xl rounded-3xl shadow-2xl border border-white/20 p-8 hover:bg-white/15 transition-all duration-300">
                <h3 class="text-2xl font-bold text-white mb-4 drop-shadow-md bg-gradient-to-r from-cyan-300 to-teal-300 bg-clip-text text-transparent">Now Playing</h3>
                <div class="overflow-x-auto overflow-y-hidden snap-x snap-mandatory scroll-smooth touch-pan-x cursor-grab" data-hscroll>
                    <div id="now-playing-row" class="flex flex-nowrap gap-x-6 pb-3 min-w-max"></div>
                </div>
            </section>
        </main>
    </div>

    <!-- JavaScript remains the same as original -->
    <script>
        // [Include all the original JavaScript functionality here]
    </script>
</body>
</html>
```

#### `theme3-arctic-header.html`
```html
<header class="fixed top-0 left-0 right-0 z-40 bg-white/10 backdrop-blur-2xl border-b border-white/20 shadow-2xl">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-16">
            <!-- Logo -->
            <div class="flex-shrink-0">
                <h1 class="text-2xl font-bold bg-gradient-to-r from-cyan-400 to-teal-400 bg-clip-text text-transparent cursor-pointer">Cinematch</h1>
            </div>

            <!-- Desktop Navigation -->
            <nav class="hidden md:flex items-center space-x-8">
                <!-- Search Bar -->
                <div class="relative bg-white/15 backdrop-blur-xl border border-white/30 rounded-2xl">
                    <input type="text" placeholder="Search movies, TV shows..." class="bg-transparent text-white border-none outline-none w-full px-4 py-2 text-sm rounded-2xl placeholder-white/70" />
                </div>

                <!-- User Dropdown -->
                <div class="user-dropdown">
                    <button class="user-button flex items-center space-x-2 text-white px-3 py-2 rounded-lg">
                        <div class="w-8 h-8 bg-gradient-to-br from-cyan-500 to-teal-600 rounded-full flex items-center justify-center text-sm font-semibold">U</div>
                        <span class="hidden lg:block text-sm font-medium">User</span>
                    </button>
                    <!-- Dropdown menu with arctic theme styling -->
                </div>
            </nav>
        </div>
    </div>
</header>
```

---

## 🚀 How to Use These Themes

### Quick Setup:

1. **Choose a theme** from the three options above
2. **Copy the HTML code** for both the index and header files
3. **Save them** with the suggested filenames
4. **Update the fetch URL** in the JavaScript to match your header filename:
   ```javascript
   fetch('theme1-sunset-header.html') // or theme2-midnight-header.html, etc.
   ```
5. **Open the index file** in your browser to see the theme

### Key Features:

- ✅ **Fully responsive** design
- ✅ **Modern glassmorphism** effects
- ✅ **Smooth animations** and transitions
- ✅ **Accessible** color contrasts
- ✅ **Cinematic** visual appeal
- ✅ **Copy-paste ready** code

### Customization Tips:

- **Adjust opacity**: Change `/20`, `/80`, etc. values for different transparency levels
- **Modify gradients**: Update `from-color via-color to-color` combinations
- **Change blur intensity**: Adjust `backdrop-blur-xl`, `backdrop-blur-2xl` values
- **Update border radius**: Modify `rounded-xl`, `rounded-2xl`, `rounded-3xl` classes

Each theme maintains the same functionality while providing a completely different visual experience perfect for a modern movie recommendation platform.