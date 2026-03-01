# Savonoppimport React from "react"; import { motion } from "framer-motion"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Phone, Mail, ShoppingCart, MessageCircle, Star } from "lucide-react";

export default function SavonOPPWebsite() { return ( <div className="min-h-screen bg-gradient-to-b from-green-50 to-white text-gray-800"> {/* HERO SECTION PREMIUM */} <section className="bg-gradient-to-r from-green-800 via-green-600 to-green-500 text-white py-24 px-6 text-center"> <motion.h1 initial={{ opacity: 0, y: -30 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.8 }} className="text-5xl md:text-7xl font-extrabold mb-6" > Savon OPP </motion.h1> <p className="text-xl md:text-2xl max-w-3xl mx-auto mb-10 leading-relaxed"> L’excellence du savon fabriqué au Bénin. Pureté, fraîcheur et qualité haut de gamme pour les ménages, marchés et grossistes. </p> <div className="flex flex-col md:flex-row gap-4 justify-center"> <Button className="bg-white text-green-800 hover:bg-gray-100 text-lg px-8 py-4 rounded-2xl shadow-2xl"> Commander Maintenant </Button> <Button className="bg-green-900 text-white hover:bg-green-950 text-lg px-8 py-4 rounded-2xl shadow-2xl flex items-center gap-2"> <MessageCircle size={20}/> WhatsApp Direct </Button> </div> </section>

{/* VALEURS */}
  <section className="py-20 px-6 max-w-6xl mx-auto">
    <h2 className="text-4xl font-bold text-center mb-14">Pourquoi choisir Savon OPP ?</h2>
    <div className="grid md:grid-cols-3 gap-10">
      {["Qualité Supérieure", "Prix Compétitif", "Fabrication Locale"].map((item, index) => (
        <Card key={index} className="rounded-2xl shadow-xl hover:shadow-2xl transition duration-300">
          <CardContent className="p-8 text-center">
            <Star className="mx-auto mb-4" size={40} />
            <h3 className="text-xl font-semibold mb-3">{item}</h3>
            <p>Un engagement fort pour satisfaire chaque client avec un produit fiable et performant.</p>
          </CardContent>
        </Card>
      ))}
    </div>
  </section>

  {/* PRODUITS PREMIUM */}
  <section className="py-20 px-6 bg-green-50">
    <h2 className="text-4xl font-bold text-center mb-14">Nos Gammes</h2>
    <div className="grid md:grid-cols-3 gap-10 max-w-6xl mx-auto">
      {["Savon Classique", "Savon Premium", "Offre Grossiste"].map((product, index) => (
        <Card key={index} className="rounded-2xl shadow-xl hover:shadow-2xl transition duration-300">
          <CardContent className="p-8 text-center">
            <div className="h-44 bg-green-200 rounded-2xl mb-6 flex items-center justify-center">
              <ShoppingCart size={45} />
            </div>
            <h3 className="text-2xl font-semibold mb-3">{product}</h3>
            <p className="mb-6">Disponible en grande quantité pour marchés, supermarchés et distributeurs.</p>
            <Button className="rounded-2xl w-full">Acheter</Button>
          </CardContent>
        </Card>
      ))}
    </div>
  </section>

  {/* SECTION GROSSISTE */}
  <section className="py-20 px-6 bg-white">
    <div className="max-w-5xl mx-auto text-center">
      <h2 className="text-4xl font-bold mb-8">Spécial Revendeurs & Grossistes</h2>
      <p className="text-lg mb-10">
        Vous êtes commerçant ou supermarché ? Profitez de nos tarifs spéciaux et d’une livraison rapide.
      </p>
      <Button className="bg-green-700 hover:bg-green-800 text-white text-lg px-10 py-4 rounded-2xl shadow-xl">
        Demander un Devis
      </Button>
    </div>
  </section>

  {/* CONTACT PREMIUM */}
  <section className="py-20 px-6 bg-green-100">
    <h2 className="text-4xl font-bold text-center mb-14">Contact Officiel</h2>
    <div className="max-w-4xl mx-auto grid md:grid-cols-2 gap-10">
      <Card className="rounded-2xl shadow-xl">
        <CardContent className="p-8">
          <h3 className="text-2xl font-semibold mb-6">Coordonnées</h3>
          <p className="flex items-center gap-3 mb-4"><Phone size={20}/> 01 92 20 80 91</p>
          <p className="flex items-center gap-3 mb-4"><Mail size={20}/> zabdielhounhouizi205@gmail.com</p>
          <p>Cotonou, Bénin</p>
        </CardContent>
      </Card>

      <Card className="rounded-2xl shadow-xl">
        <CardContent className="p-8">
          <h3 className="text-2xl font-semibold mb-6">Commande Rapide</h3>
          <Button className="w-full bg-green-800 hover:bg-green-900 text-white py-4 rounded-2xl flex items-center justify-center gap-3">
            <MessageCircle size={22}/> Commander via WhatsApp
          </Button>
        </CardContent>
      </Card>
    </div>
  </section>

  {/* FOOTER PREMIUM */}
  <footer className="bg-green-900 text-white text-center py-8">
    <p className="text-lg font-semibold">© {new Date().getFullYear()} Savon OPP</p>
    <p className="text-sm opacity-80 mt-2">Entreprise béninoise - Tous droits réservés</p>
  </footer>
</div>

); }
