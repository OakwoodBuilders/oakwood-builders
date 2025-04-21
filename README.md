import Head from "next/head";
import Image from "next/image";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { MoveRight } from "lucide-react";
import { motion } from "framer-motion";

export default function OakwoodBuilders() {
  return (
    <>
      <Head>
        <title>Oakwood Builders | Custom Homes in Southeastern Nebraska</title>
        <meta name="description" content="Oakwood Builders crafts high-quality, custom-built homes in Southeastern Nebraska. We build homes, not houses." />
        <meta name="keywords" content="custom homes, southeastern Nebraska, construction, Oakwood Builders, new home builders" />
        <meta name="author" content="Oakwood Builders" />

        <meta property="og:title" content="Oakwood Builders | Custom Homes in Southeastern Nebraska" />
        <meta property="og:description" content="We build homes, not houses. Oakwood Builders specializes in building custom homes tailored to your vision." />
        <meta property="og:image" content="/oakwood-logo-bw.jpg" />
        <meta property="og:url" content="https://oakwoodbuildersofnebraska.com" />
        <meta property="og:type" content="website" />

        <meta name="twitter:card" content="summary_large_image" />
        <meta name="twitter:title" content="Oakwood Builders | Custom Homes in Southeastern Nebraska" />
        <meta name="twitter:description" content="We build homes, not houses. Let Oakwood Builders craft your dream home." />
        <meta name="twitter:image" content="/oakwood-logo-bw.jpg" />
        <script type="application/ld+json">
          {`
          {
            "@context": "https://schema.org",
            "@type": "HomeAndConstructionBusiness",
            "name": "Oakwood Builders",
            "image": "https://oakwoodbuildersofnebraska.com/oakwood-logo-bw.jpg",
            "@id": "https://oakwoodbuilders.com",
            "url": "https://oakwoodbuilders.com",
            "telephone": "+1-402-555-1234",
            "address": {
              "@type": "PostalAddress",
              "streetAddress": "123 Oak Lane",
              "addressLocality": "Malmo",
              "addressRegion": "NE",
              "postalCode": "68040",
              "addressCountry": "US"
            },
            "geo": {
              "@type": "GeoCoordinates",
              "latitude": 41.2661,
              "longitude": -96.5739
            },
            "openingHoursSpecification": [{
              "@type": "OpeningHoursSpecification",
              "dayOfWeek": [
                "Monday",
                "Tuesday",
                "Wednesday",
                "Thursday",
                "Friday"
              ],
              "opens": "08:00",
              "closes": "17:00"
            }],
            "sameAs": [
              "https://www.facebook.com/oakwoodbuilders",
              "https://www.instagram.com/oakwoodbuilders"
            ]
          }
          `}
        </script>
        <link rel="icon" href="/oakwood-logo-bw.jpg" />
      </Head>

      <div className="p-4 md:p-10 max-w-6xl mx-auto text-navy bg-[#fdfdfc]">
        <style jsx global>{`
          :root {
            --navy: #0a1a2f;
            --gold: #d4af37;
          }
          .text-navy {
            color: var(--navy);
          }
          .bg-gold {
            background-color: var(--gold);
          }
          .text-gold {
            color: var(--gold);
          }
          .border-gold {
            border-color: var(--gold);
          }
        `}</style>

        <div className="flex justify-center mb-8">
          <Image
            src="/oakwood-logo-bw.jpg"
            alt="Oakwood Builders Logo"
            width={240}
            height={240}
            className="object-contain rounded-xl border border-navy p-2"
          />
        </div>

        <motion.h1
          initial={{ opacity: 0, y: -20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.8 }}
          className="text-4xl md:text-6xl font-bold mb-4 text-center tracking-tight"
        >
          Oakwood Builders
        </motion.h1>

        <motion.h2
          initial={{ opacity: 0 }}
          animate={{ opacity: 1 }}
          transition={{ delay: 0.2, duration: 0.6 }}
          className="text-xl md:text-2xl font-medium text-center text-gold italic mb-6"
        >
          "We build homes, not houses."
        </motion.h2>

        <motion.p
          initial={{ opacity: 0 }}
          animate={{ opacity: 1 }}
          transition={{ delay: 0.4, duration: 0.6 }}
          className="text-center max-w-2xl mx-auto text-lg mb-10 leading-relaxed"
        >
          Rooted in tradition. Driven by values. Oakwood Builders helps families across southeastern Nebraska build quality custom homes that stand the test of time. Let us turn your vision into a place your family can grow and thrive.
        </motion.p>

        <motion.div
          initial={{ opacity: 0 }}
          animate={{ opacity: 1 }}
          transition={{ delay: 0.6 }}
          className="text-center mb-16"
        >
          <Button className="text-lg px-6 py-3 rounded-2xl shadow-md bg-gold text-navy">
            Start Your Custom Home Journey
          </Button>
        </motion.div>
              <motion.div
          initial={{ opacity: 0 }}
          animate={{ opacity: 1 }}
          transition={{ delay: 0.8 }}
          className="mt-20 max-w-2xl mx-auto text-center"
        >
          <h2 className="text-3xl font-bold text-center mb-6">Contact Us</h2>
          <form action="https://script.google.com/macros/s/AKfycbxExampleRealScriptIDforGoogleSheets/exec" method="POST" onSubmit={(e) => {
            e.preventDefault();
            const form = e.target;
            const formData = new FormData(form);
            fetch(form.action, {
              method: form.method,
              body: formData,
              headers: { Accept: 'application/json' },
            })
              .then((response) => {
                if (response.ok) {
                  alert('Thanks for your message! We’ll get back to you soon.');
                  form.reset();
                } else {
                  alert('Oops! Something went wrong. Please try again.');
                }
              })
              .catch(() => alert('There was a problem submitting the form.'));
          }}>
            <Input
              name="name"
              placeholder="Name"
              required
              className="border border-gold"
            />
            <Input
              name="email"
              type="email"
              placeholder="Email"
              required
              className="border border-gold"
            />
            <Textarea
              name="message"
              placeholder="Your Message"
              required
              className="border border-gold"
              rows={5}
            />
            <Button type="submit" className="bg-gold text-navy w-full">
              Send Message
            </Button>
          </form>
        </motion.div>

        <div className="mt-12 border-t border-gray-200 pt-6 text-center text-sm text-muted-foreground">
          <p>Contact: <strong>Peter Kavan</strong></p>
          <p>Email: <a href="mailto:Oakwoodbuilderofne@gmail.com" className="text-gold underline">Oakwoodbuilderofne@gmail.com</a></p>
          <p>Phone: <a href="tel:+14024175381" className="text-gold underline">(402) 417-5381</a></p>
          <p className="mt-4">&copy; {new Date().getFullYear()} Oakwood Builders. All rights reserved.</p>
                <motion.div className="mt-24">
          <h2 className="text-3xl font-bold text-center mb-6">See Where We Build</h2>
          <div className="w-full aspect-video rounded-xl overflow-hidden shadow-md">
            <iframe
              title="Oakwood Builders Location Map"
              src="https://www.google.com/maps/embed/v1/place?q=Malmo,NE&key=AIzaSyB-oakwoodNebraskaMAPKEY1234"
              width="100%"
              height="100%"
              style={{ border: 0 }}
              loading="lazy"
              allowFullScreen
            ></iframe>
          </div>
        </motion.div>

        <motion.div className="mt-24">
          <h2 className="text-3xl font-bold text-center mb-8">Project Portfolio</h2>
          <div className="grid md:grid-cols-3 gap-4">
            {[
  { filename: 'custom-farmhouse-home-nebraska.jpg', alt: 'Custom Farmhouse Home in Nebraska by Oakwood Builders' },
  { filename: 'modern-custom-home-se-nebraska.jpg', alt: 'Modern Custom Home in Southeastern Nebraska' },
  { filename: 'colonial-style-home-build.jpg', alt: 'Colonial Style Home Built by Oakwood Builders' },
  { filename: 'craftsman-custom-build.jpg', alt: 'Craftsman Custom Home by Oakwood Builders' },
  { filename: 'ranch-style-nebraska-home.jpg', alt: 'Nebraska Ranch Style Home Construction' },
  { filename: 'two-story-dream-home.jpg', alt: 'Two Story Custom Dream Home in Nebraska' }
].map((id, i) => (
              <div key={id} className="rounded-xl overflow-hidden shadow-md">
                <Image
  loading="lazy"
  src={`/portfolio/${id.filename}`}
  alt={id.alt}
  width={600}
  height={400}
  className="w-full h-auto object-cover rounded-xl"
/>
              </div>
            ))}
          </div>
        </motion.div>

        <motion.div className="mt-24">
          <h2 className="text-3xl font-bold text-center mb-8">Happy Clients</h2>
          <div className="overflow-x-auto whitespace-nowrap scroll-smooth">
            <div className="flex gap-6 px-2">
              {[
                {
                  name: "Sarah M.",
                  text: "Oakwood Builders brought our dream to life. Honest, reliable, and local to Nebraska!",
                },
                {
                  name: "James R.",
                  text: "Professional, detailed, and friendly. Our family loves the new home!",
                },
                {
                  name: "Linda & Mark",
                  text: "We felt heard and cared for every step. So glad we chose Oakwood Builders.",
                },
              ].map((t, i) => (
                <div key={i} className="min-w-[300px] max-w-sm bg-white border border-gold text-navy rounded-2xl p-6 shadow-md">
                  <p className="mb-3">"{t.text}"</p>
                  <p className="text-sm font-semibold text-right">— {t.name}</p>
                </div>
              ))}
            </div>
          </div>
        </motion.div>

        <motion.div className="mt-24 max-w-4xl mx-auto text-center">
          <h2 className="text-3xl font-bold mb-4">Free Custom Home Planning Guide</h2>
          <p className="mb-6 text-muted-foreground">Download our printable brochure that walks you through everything you need to know about building a custom home in southeastern Nebraska.</p>
          <a
            href="/Oakwood-Custom-Home-Guide.pdf"
            download
            className="inline-block px-6 py-3 bg-gold text-navy font-medium rounded-xl shadow hover:shadow-lg"
          >
            Download PDF Brochure
          </a>
        </motion.div>

        <motion.div className="mt-24 max-w-4xl mx-auto text-center">
          <h2 className="text-3xl font-bold mb-6">Credentials & Memberships</h2>
          <ul className="text-left text-lg space-y-3">
            <li>✔️ Licensed, Bonded & Insured in Nebraska</li>
            <li>✔️ Member of the Nebraska State Home Builders Association</li>
            <li>✔️ Energy-efficient, modern building practices</li>
            <li>✔️ 10-Year Structural Warranty included</li>
          </ul>
        </motion.div>

      </div>
    </div>
  </div>
</div>
</>
  );
}
