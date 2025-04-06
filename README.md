# AnubisAx.github.io
from IPython.display import HTML, display

final_code = """
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>GRAVCOM: Упругий силовой шарнир</title>
    <style>
        :root {
            --primary: #2A5D84;
            --accent: #FF6B6B;
            --dark: #1a3650;
            --light: #f8f9fa;
        }

        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            line-height: 1.6;
            background: var(--light);
        }

        .hero {
            background: linear-gradient(45deg, var(--primary), #1a3650);
            color: white;
            padding: 8rem 1rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
            max-width: 1200px;
            margin: 4rem auto;
            padding: 0 1rem;
        }

        .feature-card {
            background: white;
            border-radius: 15px;
            padding: 2rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.15);
        }

        .specs-section {
            background: var(--dark);
            color: white;
            padding: 6rem 1rem;
        }

        .specs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 3rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .spec-card {
            background: rgba(255,255,255,0.05);
            border-radius: 20px;
            padding: 2.5rem;
            border: 1px solid rgba(255,255,255,0.1);
            transition: all 0.3s;
        }

        .spec-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .spec-value {
            font-size: 2rem;
            color: var(--accent);
            margin: 1rem 0;
        }

        .hero-image {
            width: 300px;
            margin: 2rem auto;
            display: block;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }

        @media (max-width: 768px) {
            .hero { padding: 4rem 1rem; }
            .product-grid { gap: 1.5rem; }
            .hero-image { width: 200px; }
        }
    </style>
</head>
<body>
    <section class="hero">
        <h1 style="font-size: 3.2rem; margin-bottom: 1.5rem;">
            <span style="font-weight: 300;">GRAVCOM</span><br>
            <strong>Упругий шарнир с ПСК</strong>
        </h1>
        <p style="font-size: 1.3rem; opacity: 0.9;">
            Постоянная силовая характеристика в любых условиях
        </p>
        <img src="https://via.placeholder.com/300x200.png?text=Схема+шарнира"
             class="hero-image"
             alt="3D модель шарнира">
    </section>

    <div class="product-grid">
        <div class="feature-card">
            <h3>⚡ Линейный отклик</h3>
            <p>Стабильная силовая характеристика в диапазоне ±30°</p>
        </div>

        <div class="feature-card">
            <h3>🔄 Нулевой люфт</h3>
            <p>Прецизионная точность позиционирования</p>
        </div>

        <div class="feature-card">
            <h3>🛡️ Антикоррозийная защита</h3>
            <p>Специальное вакуумное покрытие</p>
        </div>
    </div>

    <section class="specs-section">
        <div class="specs-grid">
            <div class="spec-card">
                <div class="spec-icon">⚖️</div>
                <h3>Силовые параметры</h3>
                <div class="spec-value">1500 Н·м</div>
                <p>Максимальный крутящий момент</p>
                <div class="spec-value">±5%</div>
                <p>Отклонение характеристики</p>
            </div>

            <div class="spec-card">
                <div class="spec-icon">🌡️</div>
                <h3>Эксплуатация</h3>
                <div class="spec-value">-50°C ~ +150°C</div>
                <p>Рабочий диапазон</p>
                <div class="spec-value">IP69K</div>
                <p>Защита от воздействий</p>
            </div>
        </div>
    </section>

    <script>
        const animateElements = (selector, delay = 200) => {
            document.querySelectorAll(selector).forEach((el, index) => {
                el.style.opacity = '0';
                el.style.transform = 'translateY(20px)';
                setTimeout(() => {
                    el.style.opacity = '1';
                    el.style.transform = 'translateY(0)';
                }, delay * index);
            });
        }

        window.addEventListener('load', () => {
            animateElements('.feature-card');
            animateElements('.spec-card', 300);
        });
    </script>
</body>
</html>
"""

display(HTML(final_code))
