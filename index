import { useState } from "react";
import { motion } from "framer-motion";
import { MapPin, Dumbbell, Globe2, Smartphone, QrCode, CreditCard, ArrowRight } from "lucide-react";
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const nav = [
  { href: "#features", label: "Features" },
  { href: "#how", label: "How It Works" },
  { href: "#pricing", label: "Pricing" },
  { href: "#faq", label: "FAQ" },
];

export default function NomadLyftLanding() {
  const [mobileOpen, setMobileOpen] = useState(false);
  return (
    <div className="min-h-screen bg-gradient-to-b from-amber-50 via-white to-white text-slate-900">
      <header className="sticky top-0 z-50 bg-white/80 backdrop-blur border-b">
        <div className="max-w-6xl mx-auto px-4 py-3 flex items-center justify-between gap-3">
          <div className="flex items-center gap-3">
            <div className="h-9 w-9 rounded-xl bg-violet-600 grid place-items-center text-white font-bold">N</div>
            <span className="font-semibold tracking-tight">NomadLyft</span>
          </div>
          <nav className="hidden md:flex items-center gap-6 text-sm">
            {nav.map((n) => (
              <a key={n.href} href={n.href} className="hover:text-violet-700 transition-colors">
                {n.label}
              </a>
            ))}
            <Button className="rounded-2xl">Create free account</Button>
          </nav>
          <button onClick={() => setMobileOpen((v) => !v)} className="md:hidden inline-flex items-center p-2 rounded-xl border">
            <span className="sr-only">Toggle Menu</span>
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><line x1="3" y1="12" x2="21" y2="12"></line><line x1="3" y1="6" x2="21" y2="6"></line><line x1="3" y1="18" x2="21" y2="18"></line></svg>
          </button>
        </div>
        {mobileOpen && (
          <div className="md:hidden border-t bg-white">
            <div className="max-w-6xl mx-auto px-4 py-2 grid gap-2">
              {nav.map((n) => (
                <a key={n.href} href={n.href} className="py-2" onClick={() => setMobileOpen(false)}>
                  {n.label}
                </a>
              ))}
              <Button className="rounded-2xl w-full mt-2">Create free account</Button>
            </div>
          </div>
        )}
      </header>

      <section className="relative bg-[url('/hero-bg.jpg')] bg-cover bg-center">
        <div className="max-w-6xl mx-auto px-4 pt-16 pb-24 grid md:grid-cols-2 gap-10 items-center bg-white/70 backdrop-blur rounded-3xl">
          <div>
            <motion.h1 initial={{opacity:0, y:10}} whileInView={{opacity:1, y:0}} viewport={{once:true}} className="text-4xl md:text-6xl font-extrabold tracking-tight">
              Train <span className="text-violet-700">Everywhere</span>
            </motion.h1>
            <p className="mt-4 text-lg text-slate-600 max-w-prose">
              A global fitness app for travelers and nomads. Find gyms near you, buy a pass, and check in with a QR code—no contracts.
            </p>
            <div className="mt-6 flex flex-wrap gap-3">
              <Button size="lg" className="rounded-2xl">
                Find gyms near me <ArrowRight className="ml-2 h-4 w-4"/>
              </Button>
              <a href="#pricing" className="px-5 py-2.5 rounded-2xl border font-medium hover:bg-slate-50">See pricing</a>
            </div>
          </div>
          <Card className="rounded-2xl overflow-hidden">
            <CardHeader>
              <CardTitle className="flex items-center gap-2"><Smartphone className="h-5 w-5"/>App Preview</CardTitle>
            </CardHeader>
            <CardContent className="grid gap-4">
              <div className="grid md:grid-cols-3 gap-3">
                <img src="/preview-countries.png" alt="Countries" className="aspect-[9/19] rounded-2xl border object-cover"/>
                <img src="/preview-gyms.png" alt="Gyms List" className="aspect-[9/19] rounded-2xl border object-cover"/>
                <img src="/preview-map.png" alt="Map" className="aspect-[9/19] rounded-2xl border object-cover"/>
              </div>
            </CardContent>
          </Card>
        </div>
      </section>

      <section id="features" className="py-20 bg-white">
        <div className="max-w-6xl mx-auto px-4 grid md:grid-cols-3 gap-6">
          <Card className="rounded-2xl shadow-lg">
            <CardHeader>
              <CardTitle className="flex items-center gap-2"><Dumbbell className="h-5 w-5"/>Contract‑Free Access</CardTitle>
            </CardHeader>
            <CardContent className="text-slate-600">Buy day or multi‑day passes without paperwork or long‑term commitments.</CardContent>
          </Card>
          <Card className="rounded-2xl shadow-lg">
            <CardHeader>
              <CardTitle className="flex items-center gap-2"><Globe2 className="h-5 w-5"/>Gyms Worldwide</CardTitle>
            </CardHeader>
            <CardContent className="text-slate-600">Discover quality gyms in popular cities—perfect for travel or nomad life.</CardContent>
          </Card>
          <Card className="rounded-2xl shadow-lg">
            <CardHeader>
              <CardTitle className="flex items-center gap-2"><QrCode className="h-5 w-5"/>QR Check‑In</CardTitle>
            </CardHeader>
            <CardContent className="text-slate-600">Checkout securely, receive a QR code, and start training in seconds.</CardContent>
          </Card>
        </div>
      </section>

      {/* Keep rest of sections unchanged */}
    </div>
  );
}
