<script lang="ts">
    import { Button } from "$lib/components/ui/button/index.js";
    import { Input } from "$lib/components/ui/input/index.js";
    import { Label } from "$lib/components/ui/label/index.js";
    import Checkbox from "$lib/components/ui/checkbox/checkbox.svelte";
    import Mail from "@lucide/svelte/icons/mail";
    import Lock from "@lucide/svelte/icons/lock";
    import Infinity from "@lucide/svelte/icons/infinity";
    import Zap from "@lucide/svelte/icons/zap";
    import Shield from "@lucide/svelte/icons/shield";
    import Activity from "@lucide/svelte/icons/activity";
</script>

<div class="flex h-screen w-full">
    <div class="flex w-full lg:w-1/2 items-center justify-center p-8">
        <div class="w-full max-w-sm">
            <img
                src="/logo/logo-csfx.svg"
                alt="CSFX Logo"
                class="size-20 mb-6 rounded-md p-2 invert dark:invert-0"
            />
            <h1 class="text-2xl font-font-light mb-10">Sign in</h1>

            <div class="flex flex-col gap-1 mb-4">
                <Label for="email" class="text-xs font-bold mb-1"
                    >Email Address</Label
                >
                <div class="relative">
                    <Mail
                        class="absolute left-3 top-1/2 -translate-y-1/2 text-color-foreground size-4"
                    />
                    <Input
                        id="email"
                        type="email"
                        placeholder="you@example.com"
                        class="pl-9 pt-2 pb-2"
                    />
                </div>
            </div>

            <div class="flex flex-col gap-1 mb-4">
                <Label for="password" class="text-xs font-bold mb-1"
                    >Password</Label
                >
                <div class="relative">
                    <Lock
                        class="absolute left-3 top-1/2 -translate-y-1/2 size-4 text-color-foreground"
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

            <Button class="w-full">Sign in</Button>
        </div>
    </div>

    <div class="hidden lg:flex lg:w-1/2 p-6">
        <div
            class="relative w-full rounded-3xl overflow-hidden flex flex-col justify-between p-10"
        >
            <img
                src="/gradients/Gradient-dark.svg"
                alt=""
                class="absolute inset-0 w-full h-full object-cover dark:hidden"
            />
            <img
                src="/gradients/Gradient-light.svg"
                alt=""
                class="absolute inset-0 w-full h-full object-cover hidden dark:block"
            />

            <div class="absolute inset-0 pointer-events-none overflow-hidden">
                <div
                    class="absolute -top-20 left-1/3 w-px h-[140%] bg-white/5 rotate-12 blur-sm"
                ></div>
                <div
                    class="absolute -top-20 left-1/2 w-px h-[140%] bg-white/5 rotate-12 blur-sm"
                ></div>
                <div
                    class="absolute -top-20 right-1/4 w-px h-[140%] bg-white/5 rotate-12 blur-sm"
                ></div>
            </div>

            <img
                src="/logo/logo-csfx.svg"
                alt=""
                class="absolute -top-10 -right-16 w-96 opacity-[0.12] pointer-events-none select-none"
                aria-hidden="true"
            />

            <div class="relative z-10 flex items-center gap-3"></div>

            <div class="relative z-10">
                <p
                    class="text-panel-foreground/50 text-xs uppercase tracking-widest mb-4 font-medium"
                >
                    CSFX Hypervisor
                </p>
                <h2
                    class="text-panel-foreground text-5xl font-bold leading-tight mb-5 tracking-tight"
                >
                    Welcome<br />to CSFX
                </h2>
                <p
                    class="text-panel-foreground/60 text-sm leading-relaxed max-w-xs mb-3"
                >
                    Orchestrate and manage your entire cloud infrastructure from
                    a single hypervisor platform.
                </p>
                <p class="text-panel-foreground/40 text-xs">
                    Trusted by teams running mission-critical workloads
                </p>
            </div>

            <div class="relative z-10">
                <div
                    class="relative bg-panel-foreground/10 border border-panel-foreground/10 backdrop-blur-sm p-6 rounded-2xl"
                >
                    <div class="grid grid-cols-2 gap-5">
                        <div class="flex flex-col gap-2">
                            <Infinity class="size-4 text-panel-foreground/70" />
                            <span
                                class="text-panel-foreground text-xs font-semibold"
                                >Orchestration</span
                            >
                            <span
                                class="text-panel-foreground/50 text-xs leading-relaxed"
                                >Deploy and scale workloads across any cloud</span
                            >
                        </div>
                        <div class="flex flex-col gap-2">
                            <Zap class="size-4 text-panel-foreground/70" />
                            <span
                                class="text-panel-foreground text-xs font-semibold"
                                >Hypervisor Layer</span
                            >
                            <span
                                class="text-panel-foreground/50 text-xs leading-relaxed"
                                >Bare-metal performance with VM flexibility</span
                            >
                        </div>
                        <div class="flex flex-col gap-2">
                            <Shield class="size-4 text-panel-foreground/70" />
                            <span
                                class="text-panel-foreground text-xs font-semibold"
                                >Isolation</span
                            >
                            <span
                                class="text-panel-foreground/50 text-xs leading-relaxed"
                                >Secure tenancy with strict resource boundaries</span
                            >
                        </div>
                        <div class="flex flex-col gap-2">
                            <Activity class="size-4 text-panel-foreground/70" />
                            <span
                                class="text-panel-foreground text-xs font-semibold"
                                >Observability</span
                            >
                            <span
                                class="text-panel-foreground/50 text-xs leading-relaxed"
                                >Full-stack metrics, logs, and tracing built-in</span
                            >
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
