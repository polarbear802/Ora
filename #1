import React, { useState } from 'react';

const OrangiApp = () => {
  const [currentScreen, setCurrentScreen] = useState('inicio');
  const [menuOpen, setMenuOpen] = useState(false);
  const [cartCount, setCartCount] = useState(0);

  const menuItems = [
    {
      id: 1,
      name: 'Orange Chicken Estilo Americano',
      price: 30.00,
      description: 'Nuestro icónico pollo: una explosión de sabor donde el fuerte carácter de la naranja natural se encuentra con un apanado perfecto. Disfruta de un bocado intensamente crujiente por fuera, mientras descubres un interior tierno, jugoso y lleno de sabor. Acompañado de nuestro exclusivo arroz al estilo chino con sutiles toques de cebollín fresco.',
      image: 'https://images.unsplash.com/photo-1525755662778-989d0524087e?auto=format&fit=crop&w=800&q=80',
    },
    {
      id: 2,
      name: 'Res al Wok con Tricolor de Pimentones',
      price: 28.00,
      description: 'Tiernos cortes de res seleccionada, salteados al fuego intenso de nuestro wok para lograr ese ahumado inconfundible. Combinamos la intensidad de la carne con la frescura crujiente de pimentones rojos, amarillos y verdes, creando una danza de colores y texturas. Sazonada con nuestro secreto fraternal.',
      image: 'https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&w=800&q=80',
    }
  ];

  return (
    <div style={styles.container}>
      <nav style={styles.navbar}>
        <h1 style={styles.logo} onClick={() => setCurrentScreen('inicio')}>ORANGI</h1>
        <button style={styles.menuBtn} onClick={() => setMenuOpen(!menuOpen)}>MENU</button>
      </nav>

      {menuOpen && (
        <div style={styles.drawer}>
          <button style={styles.navLink} onClick={() => {setCurrentScreen('inicio'); setMenuOpen(false);}}>INICIO</button>
          <button style={styles.navLink} onClick={() => {setCurrentScreen('platillos'); setMenuOpen(false);}}>PLATILLOS</button>
          <button style={styles.navLink} onClick={() => {setCurrentScreen('miembros'); setMenuOpen(false);}}>MIEMBROS</button>
        </div>
      )}

      <main style={styles.main}>
        {currentScreen === 'inicio' && (
          <div style={styles.center}>
            <h2 style={styles.title}>Alta cocina de hogar</h2>
            <p style={styles.text}>Cada plato es preparado con dedicación y el calor de nuestra familia.</p>
          </div>
        )}

        {currentScreen === 'platillos' && (
          <div>
            {menuItems.map(item => (
              <div key={item.id} style={styles.card}>
                <img src={item.image} style={styles.img} alt={item.name} />
                <div style={styles.pad}>
                  <h3 style={styles.cardTitle}>{item.name}</h3>
                  <p style={styles.desc}>{item.description}</p>
                  <p style={styles.price}>Bs. {item.price.toFixed(2)}</p>
                </div>
              </div>
            ))}
          </div>
        )}

        {currentScreen === 'miembros' && (
          <div style={styles.center}>
            <h2 style={styles.title}>La Orange Card</h2>
            <div style={styles.memberCard}>
              <p>ORANGI MEMBER</p>
              <p>Refresco ilimitado al mes</p>
            </div>
            <p style={styles.stat}>185 personas ya son miembros.</p>
          </div>
        )}
      </main>
    </div>
  );
};

const styles = {
  container: { backgroundColor: '#000', color: '#fff', minHeight: '100vh', fontFamily: 'Arial' },
  navbar: { display: 'flex', justifyContent: 'space-between', padding: '20px', borderBottom: '1px solid #d32f2f' },
  logo: { color: '#d32f2f', cursor: 'pointer', fontSize: '24px' },
  menuBtn: { background: '#e65100', border: 'none', color: '#fff', padding: '10px 20px', cursor: 'pointer' },
  drawer: { background: '#111', padding: '20px', display: 'flex', flexDirection: 'column' },
  navLink: { background: 'none', border: 'none', color: '#fff', padding: '15px', textAlign: 'left', cursor: 'pointer' },
  main: { maxWidth: '800px', margin: '0 auto', padding: '20px' },
  center: { textAlign: 'center' },
  title: { color: '#d32f2f', fontSize: '32px' },
  card: { background: '#111', borderRadius: '10px', overflow: 'hidden', marginBottom: '20px' },
  img: { width: '100%', height: '200px', objectFit: 'cover' },
  pad: { padding: '20px' },
  cardTitle: { color: '#ffcc00', margin: '0 0 10px 0' },
  desc: { color: '#ccc', fontSize: '14px', lineHeight: '1.6' },
  price: { color: '#e65100', fontSize: '20px', fontWeight: 'bold' },
  memberCard: { background: '#1a0000', border: '2px solid #d32f2f', padding: '40px', margin: '20px 0' },
  stat: { color: '#ffcc00', fontWeight: 'bold' },
  text: { color: '#ccc' }
};

export default OrangiApp;
