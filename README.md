# Mesay_G
Himma Menu
HimmaCoffeeMenu() {
  const sections = [
    {
      title: 'Breakfast',
      items: [
        ['Scrambled Egg', '230'],
        ['Special Omelet', '300'],
        ['Normal Ful', '230'],
        ['Special Ful', '290'],
        ['Normal Chechebsa', '260'],
        ['Aja Chechebsa', '390'],
        ['Teff Chechebsa', '300'],
        ['Normal Fetira', '220'],
        ['Special Fetira', '350'],
      ],
    },
    {
      title: 'Sandwich & Pizza',
      items: [
        ['Chicken Club Sandwich', '440'],
        ['Tuna Club Sandwich', '480'],
        ['Vegetable Sandwich', '225'],
        ['Special Pizza', '645'],
        ['Chicken Pizza', '530'],
        ['Margherita Pizza', '450'],
      ],
    },
    {
      title: 'Juices & Smoothies',
      items: [
        ['Himma Special Juice', '310'],
        ['Apple Special', '280'],
        ['Papaya Juice', '170'],
        ['Avocado Shake', '210'],
        ['Mango Smoothie', '210'],
        ['Fruit Punch', '420'],
      ],
    },
    {
      title: 'Coffee & Drinks',
      items: [
        ['Coffee', '70'],
        ['Macchiato', '90'],
        ['Cappuccino', '150'],
        ['Caramel Macchiato', '150'],
        ['Espresso', '55'],
        ['Cold Brew', '180'],
      ],
    },
    {
      title: 'Cakes & Pastries',
      items: [
        ['Croissant', '90'],
        ['Tiramisu', '120'],
        ['Blackforest Cake', '120'],
        ['Chocolate Cake', '120'],
        ['Donut', '80'],
      ],
    },
  ];

  return (
    <div className="min-h-screen bg-[#f8f5f0] text-gray-800">
      <div className="bg-white shadow-md sticky top-0 z-10">
        <div className="max-w-6xl mx-auto px-6 py-6 flex flex-col items-center">
          <h1 className="text-5xl font-extrabold text-green-700 tracking-wide">
            Himma Coffee
          </h1>
          <p className="text-lg text-amber-700 mt-2">
            Fresh Coffee • Delicious Food • Cozy Atmosphere
          </p>
        </div>
      </div>

      <section className="max-w-6xl mx-auto px-6 py-12 grid md:grid-cols-2 gap-8">
        {sections.map((section) => (
          <div
            key={section.title}
            className="bg-white rounded-3xl shadow-lg p-6 border border-gray-100"
          >
            <h2 className="text-3xl font-bold text-green-700 mb-6 border-b pb-3">
              {section.title}
            </h2>

            <div className="space-y-4">
              {section.items.map(([item, price]) => (
                <div
                  key={item}
                  className="flex justify-between items-center text-lg"
                >
                  <span>{item}</span>
                  <span className="font-bold text-amber-700">{price} ETB</span>
                </div>
              ))}
            </div>
          </div>
        ))}
      </section>

      <footer className="bg-green-700 text-white mt-10">
        <div className="max-w-6xl mx-auto px-6 py-8 text-center space-y-2">
          <p className="text-xl font-semibold">Himma Coffee</p>
          <p>Lideta, Teklehaimanot, Addis Ababa</p>
          <p>09359882 / 0911123830</p>
          <p>ourhimma@gmail.com</p>
        </div>
      </footer>
    </div>
  );
}
