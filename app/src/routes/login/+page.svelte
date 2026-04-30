<script lang="ts">
    import { Button } from "$lib/components/ui/button/index.js";
    import { Input } from "$lib/components/ui/input/index.js";
    import { Label } from "$lib/components/ui/label/index.js";
    import Checkbox from "$lib/components/ui/checkbox/checkbox.svelte";
    import Mail from "@lucide/svelte/icons/mail";
    import Lock from "@lucide/svelte/icons/lock";
    import TrendingUp from "@lucide/svelte/icons/trending-up";
</script>

<div class="flex h-screen w-full">
    <!-- Left: Login Form -->
    <div class="flex w-full lg:w-1/2 items-center justify-center p-8">
        <div class="w-full max-w-sm">
            <h1 class="text-2xl font-bold mb-2">Welcome Back!</h1>
            <p class="text-muted-foreground mb-6">
                Please login to your account
            </p>

            <div class="flex flex-col gap-1 mb-4">
                <Label for="email">Email Address</Label>
                <div class="relative">
                    <Mail
                        class="absolute left-3 top-1/2 -translate-y-1/2 text-muted-foreground size-4"
                    />
                    <Input
                        id="email"
                        type="email"
                        placeholder="you@example.com"
                        class="pl-9"
                    />
                </div>
            </div>

            <div class="flex flex-col gap-1 mb-4">
                <Label for="password">Password</Label>
                <div class="relative">
                    <Lock
                        class="absolute left-3 top-1/2 -translate-y-1/2 text-muted-foreground size-4"
                    />
                    <Input
                        id="password"
                        type="password"
                        placeholder="••••••••"
                        class="pl-9"
                    />
                </div>
            </div>

            <div class="flex items-center gap-2 mb-6">
                <Checkbox id="remember" />
                <Label for="remember" class="cursor-pointer font-normal"
                    >Remember me</Label
                >
            </div>

            <Button class="w-full">Login</Button>
        </div>
    </div>

    <!-- Right: Promo Panel -->
    <div class="hidden lg:flex lg:w-1/2 p-6">
        <div
            class="relative w-full rounded-2xl bg-zinc-900 overflow-hidden flex flex-col justify-between p-10"
        >
            <!-- Background glow -->
            <div
                class="absolute inset-0 bg-gradient-to-br from-zinc-800 via-zinc-900 to-black opacity-80 pointer-events-none"
            ></div>
            <div
                class="absolute -top-24 -right-24 w-96 h-96 rounded-full bg-zinc-700 opacity-20 blur-3xl pointer-events-none"
            ></div>

            <!-- Top: Logo + Brand -->
            <div class="relative z-10 flex items-center gap-3">
                <div
                    class="size-8 rounded-md bg-white flex items-center justify-center"
                >
                    <TrendingUp class="size-5 text-zinc-900" />
                </div>
                <span class="text-white font-semibold text-lg">CSFX</span>
            </div>

            <!-- Middle: Main copy -->
            <div class="relative z-10">
                <p class="text-zinc-400 text-sm mb-3">Your trading platform</p>
                <h2 class="text-white text-4xl font-bold leading-tight mb-4">
                    Welcome to CSFX
                </h2>
                <p class="text-zinc-400 text-sm leading-relaxed mb-2">
                    Professional trading tools built for speed and precision.
                    Start trading smarter today.
                </p>
                <p class="text-zinc-500 text-sm">
                    More than 1k traders joined us — it's your turn
                </p>
            </div>

            <!-- Bottom card -->
            <div
                class="relative z-10 rounded-xl bg-zinc-800/80 border border-zinc-700 p-5"
            >
                <p class="text-white font-semibold text-base mb-1">
                    Trade smarter, not harder
                </p>
                <p class="text-zinc-400 text-sm">
                    Access real-time data, powerful charts, and a clean
                    interface — all in one place.
                </p>
                <!-- Avatar group -->
                <div class="flex items-center gap-2 mt-4">
                    <div class="flex -space-x-2">
                        {#each ["bg-blue-500", "bg-emerald-500", "bg-violet-500", "bg-rose-500"] as color}
                            <div
                                class="size-7 rounded-full border-2 border-zinc-800 {color}"
                            ></div>
                        {/each}
                    </div>
                    <span class="text-zinc-400 text-xs">+1k traders active</span
                    >
                </div>
            </div>
        </div>
    </div>
</div>
