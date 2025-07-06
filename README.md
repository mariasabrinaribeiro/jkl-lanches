# jkl-lanches-site
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JKL Lanches - Sabor de Verdade!</title>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Anton&family=Poppins:wght@400;700&display=swap" rel="stylesheet">





    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>

    <style>
        /* Estilos personalizados para complementar o Tailwind */
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #F5EBDC 60%, #FFE5B4 100%);
            line-height: 1.6;
        }
        .font-anton {
            font-family: 'Anton', sans-serif;
            letter-spacing: 1.5px;
        }
        .hero-bg {
            background-image: url('https://placehold.co/1200x600/D2691E/FFFFFF?text=JKL+Lanches');
            background-size: cover;
            background-position: center;
        }
        .card {
            background-color: #FFFFFF;
            border: 1px solid #EAE0D5;
            box-shadow: 0 4px 8px rgba(0,0,0,0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 22px rgba(0,0,0,0.15);
        }
        .btn-order, .btn-finalize {
            background-color: #FF8C00;
            color: white;
            font-weight: bold;
            padding: 12px 24px;
            border-radius: 9999px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            transition: all 0.2s ease-in-out;
            cursor: pointer;
            border: none;
        }
        .btn-order:hover, .btn-finalize:hover {
            background-color: #E57200;
            box-shadow: 0 6px 8px rgba(0,0,0,0.15);
            transform: translateY(-2px);
        }
        .btn-order:active, .btn-finalize:active {
            transform: translateY(0px) scale(0.98);
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        .btn-order:focus-visible, .btn-finalize:focus-visible {
            outline: 3px solid #E57200;
            outline-offset: 2px;
        }
        .btn-finalize {
            width: 100%;
        }
        #cart-sidebar {
            transition: transform 0.3s ease-in-out;
        }
        .cart-item-controls button {
            width: 30px;
            height: 30px;
            line-height: 30px;
        }
    </style>
</head>
<body class="text-stone-900 flex flex-col min-h-screen">

    <!-- Header -->
    <header class="bg-white shadow-md sticky top-0 z-20">
        <div class="container mx-auto px-4 sm:px-6 py-3 flex justify-between items-center">
            <h1 class="text-3xl md:text-4xl font-anton text-orange-600">JKL Lanches</h1>
            <div class="relative">
                <button id="cart-button" class="p-2 rounded-full hover:bg-gray-200 transition-colors">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-stone-700" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
                    </svg>
                </button>
                <span id="cart-counter" class="absolute -top-1 -right-1 bg-orange-500 text-white text-xs font-bold rounded-full h-5 w-5 flex items-center justify-center hidden">0</span>
            </div>
        </div>
    </header>

    <!-- Conteúdo Principal que se expande -->
    <div class="flex-grow">
        <!-- Seção Principal (Hero) -->
        <section class="hero-bg text-white">
            <div class="bg-black bg-opacity-50 h-full">
                <div class="container mx-auto px-4 sm:px-6 py-20 md:py-24 text-center">
                    <h2 class="text-4xl md:text-6xl font-anton mb-2 uppercase">Sabor de Verdade!</h2>
                    <p class="text-lg md:text-xl">Feito na brasa, montado na hora. Do nosso jeito.</p>
                </div>
            </div>
        </section>

        <!-- Seção do Menu -->
        <main id="menu" class="container mx-auto px-4 sm:px-6 py-12">
            
            <div class="text-center mb-12">
                <h2 class="text-4xl md:text-5xl font-anton text-stone-800 uppercase">Nosso Cardápio</h2>
            </div>

            <!-- Categoria: Café da Manhã & Salgados -->
            <section class="mb-16">
                <h3 class="text-2xl md:text-3xl font-anton border-l-8 border-orange-500 pl-4 mb-8">Café da Manhã & Salgados</h3>
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
                    <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/D2B48C/4A2311?text=P%C3%A3o+na+Chapa" alt="Imagem de Pão com manteiga na chapa" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Pão na Chapa</h4><p class="text-stone-700 text-sm mb-4">Pão de leite fatiado com manteiga na chapa, quentinho e crocante.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 7,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Pão na Chapa', 7.00)">Adicionar</button></div></div>
                    <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/FF7F50/FFFFFF?text=Bauru" alt="Imagem de Bauru" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Bauru</h4><p class="text-stone-700 text-sm mb-4">Pão de leite, presunto, queijo derretido, tomate e orégano.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 14,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Bauru', 14.00)">Adicionar</button></div></div>
                    <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/FFA07A/FFFFFF?text=Misto+Quente" alt="Imagem de Misto Quente" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Misto Quente</h4><p class="text-stone-700 text-sm mb-4">O clássico pão de leite com presunto e queijo na chapa.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 12,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Misto Quente', 12.00)">Adicionar</button></div></div>
                    <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/E9967A/FFFFFF?text=Bauregg" alt="Imagem de Bauregg" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Bauregg</h4><p class="text-stone-700 text-sm mb-4">Bauru turbinado com um ovo no ponto perfeito.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 16,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Bauregg', 16.00)">Adicionar</button></div></div>
                    <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/CD853F/FFFFFF?text=Coxinha" alt="Imagem de Coxinha" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Coxinha</h4><p class="text-stone-700 text-sm mb-4">Salgado clássico com recheio cremoso de frango.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 8,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Coxinha', 8.00)">Adicionar</button></div></div>
                    <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/A0522D/FFFFFF?text=Risole" alt="Imagem de Risole" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Risole</h4><p class="text-stone-700 text-sm mb-4">Consulte o sabor do dia.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 8,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Risole', 8.00)">Adicionar</button></div></div>
                    <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/8B4513/FFFFFF?text=Enroladinho" alt="Imagem de Enrolado de vina" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Enrolado de Vina</h4><p class="text-stone-700 text-sm mb-4">Salsicha envolta em massa macia e assada.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 8,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Enrolado de vina', 8.00)">Adicionar</button></div></div>
                </div>
            </section>

            <!-- Categoria: Bebidas Quentes -->
            <section class="mb-16">
                <h3 class="text-2xl md:text-3xl font-anton border-l-8 border-orange-500 pl-4 mb-8">Bebidas Quentes</h3>
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
                    <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/6B4F4B/FFFFFF?text=Caf%C3%A9+com+Leite" alt="Imagem de Café coado com leite" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Café com Leite</h4><p class="text-stone-700 text-sm mb-4">Café coado na hora com leite vaporizado (180ml).</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 5,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Café com Leite', 5.00)">Adicionar</button></div></div>
                    <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/4E3629/FFFFFF?text=Chocolate+Quente" alt="Imagem de Chocolate Quente" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Chocolate Quente</h4><p class="text-stone-700 text-sm mb-4">Cremoso e perfeito para aquecer o dia.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 5,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Chocolate Quente', 5.00)">Adicionar</button></div></div>
                    <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/C2B280/4A2311?text=Ch%C3%A1+Quente" alt="Imagem de Chá Quente" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Chá Quente</h4><p class="text-stone-700 text-sm mb-4">Sabores: Pêssego, Camomila, Mate Leão.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 5,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Chá Quente', 5.00)">Adicionar</button></div></div>
                </div>
            </section>

            <!-- Categoria: Açaí -->
            <section class="mb-16">
                <h3 class="text-2xl md:text-3xl font-anton border-l-8 border-orange-500 pl-4 mb-8">Açaí</h3>
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
                    <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/4B0082/FFFFFF?text=A%C3%A7a%C3%AD+300ml" alt="Imagem de Açaí no copo 300ml" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Açaí no Copo 300ml</h4><p class="text-stone-700 text-sm mb-4">A dose perfeita de energia para continuar o seu dia.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 19,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Açaí no Copo 300ml', 19.00)">Adicionar</button></div></div>
                    <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/800080/FFFFFF?text=A%C3%A7a%C3%AD+500ml" alt="Imagem de Açaí no copo 500ml" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Açaí no Copo 500ml</h4><p class="text-stone-700 text-sm mb-4">Para quem ama açaí e não tem medo de ser feliz.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 29,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Açaí no Copo 500ml', 29.00)">Adicionar</button></div></div>
                </div>
            </section>

            <!-- Categoria: Sorvetes -->
            <section class="mb-16">
                <h3 class="text-2xl md:text-3xl font-anton border-l-8 border-orange-500 pl-4 mb-8">Sorvetes e Picolés</h3>
                <div class="mb-8">
                    <h4 class="text-xl md:text-2xl font-bold text-stone-800 mb-4">Picolés Tradicionais (Fruta)</h4>
                    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
                        <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/9ACD32/FFFFFF?text=Lim%C3%A3o" alt="Picolé de Limão" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Picolé de Limão</h4><p class="text-stone-700 text-sm mb-4">Refrescante e cítrico.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 3,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Picolé de Limão', 3.00)">Adicionar</button></div></div>
                        <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/8A2BE2/FFFFFF?text=Uva" alt="Picolé de Uva" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Picolé de Uva</h4><p class="text-stone-700 text-sm mb-4">O sabor clássico da infância.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 3,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Picolé de Uva', 3.00)">Adicionar</button></div></div>
                    </div>
                </div>
                <div class="mb-8">
                    <h4 class="text-xl md:text-2xl font-bold text-stone-800 mb-4">Picolés de Leite</h4>
                    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
                        <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/FFF5EE/333333?text=Nata" alt="Picolé de Nata" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Picolé de Nata</h4><p class="text-stone-700 text-sm mb-4">Cremoso e suave.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 4,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Picolé de Nata', 4.00)">Adicionar</button></div></div>
                        <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/8B4513/FFFFFF?text=Chocolate" alt="Picolé de Chocolate" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Picolé de Chocolate</h4><p class="text-stone-700 text-sm mb-4">Intenso e cremoso.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 4,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Picolé de Chocolate', 4.00)">Adicionar</button></div></div>
                    </div>
                </div>
                 <div>
                    <h4 class="text-xl md:text-2xl font-bold text-stone-800 mb-4">Picolés Especiais</h4>
                    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
                        <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/4A2311/FFFFFF?text=Brigadeiro" alt="Picolé de Brigadeiro" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Picolé de Brigadeiro</h4><p class="text-stone-700 text-sm mb-4">Com granulado de verdade.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 6,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Picolé de Brigadeiro', 6.00)">Adicionar</button></div></div>
                        <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/FF69B4/FFFFFF?text=Sensa%C3%A7%C3%A3o" alt="Picolé Sensação" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Picolé Sensação</h4><p class="text-stone-700 text-sm mb-4">A combinação perfeita de morango e chocolate.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 6,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Picolé Sensação', 6.00)">Adicionar</button></div></div>
                        <div class="card rounded-lg overflow-hidden text-center"><img src="https://placehold.co/600x400/2F4F4F/FFFFFF?text=Skimo" alt="Picolé Skimo" class="w-full h-48 object-cover" loading="lazy"><div class="p-6"><h4 class="font-bold text-xl mb-2">Picolé Skimo</h4><p class="text-stone-700 text-sm mb-4">Casquinha de chocolate crocante por fora, cremoso por dentro.</p><div class="font-bold text-xl md:text-2xl text-stone-800 mb-4">R$ 6,00</div><button class="btn-order" onclick="adicionarAoCarrinho('Picolé Skimo', 6.00)">Adicionar</button></div></div>
                    </div>
                </div>
            </section>
        </main>
    </div>

    <!-- Footer -->
    <footer class="bg-stone-900 text-white">
        <div class="container mx-auto px-6 py-8 text-center">
            <h3 class="text-4xl font-anton text-orange-500">JKL Lanches</h3>
            <div class="mt-4 space-y-2">
                <p>
                    <a href="https://g.co/kgs/j7jMFyX" target="_blank" rel="noopener noreferrer" class="hover:text-orange-400 transition-colors inline-flex items-center">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd" /></svg>
                        Rua Castro, 110 - Caiobá
                    </a>
                </p>
                <div class="text-gray-300">
                    <p class="font-bold">Horário de Funcionamento:</p>
                    <p>Terça a Domingo: 09:00 - 23:00</p>
                    <p>Segunda-feira: 18:00 - 22:30</p>
                </div>
            </div>
            <p class="text-sm mt-6 text-gray-400">&copy; 2025 - Todos os direitos reservados.</p>
        </div>
    </footer>

    <!-- Sidebar do Carrinho -->
    <div id="cart-sidebar" class="fixed top-0 right-0 h-full w-full sm:w-96 bg-white shadow-2xl z-30 transform translate-x-full">
        <div class="flex flex-col h-full">
            <div class="flex justify-between items-center p-4 border-b">
                <h2 class="text-2xl font-anton text-stone-800">Seu Pedido</h2>
                <button id="close-cart-button" class="p-2 rounded-full hover:bg-gray-200">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" /></svg>
                </button>
            </div>
            <div id="cart-items" class="flex-grow p-4 overflow-y-auto"></div>
            <div class="p-4 border-t bg-gray-50">
                <div class="flex justify-between items-center mb-4">
                    <span class="text-lg font-bold">Total:</span>
                    <span id="cart-total" class="text-xl font-bold text-orange-600">R$ 0,00</span>
                </div>
                <button id="finalize-order-button" class="w-full btn-finalize">Finalizar Pedido via WhatsApp</button>
            </div>
        </div>
    </div>
    <div id="cart-overlay" class="fixed inset-0 bg-black bg-opacity-50 z-20 hidden"></div>

    <!-- Script do Carrinho de Compras -->
    <script>
        const cartButton = document.getElementById('cart-button');
        const closeCartButton = document.getElementById('close-cart-button');
        const cartSidebar = document.getElementById('cart-sidebar');
        const cartOverlay = document.getElementById('cart-overlay');
        const cartItemsContainer = document.getElementById('cart-items');
        const cartTotalElement = document.getElementById('cart-total');
        const cartCounterElement = document.getElementById('cart-counter');
        const finalizeOrderButton = document.getElementById('finalize-order-button');

        let cart = [];

        function toggleCart() {
            cartSidebar.classList.toggle('translate-x-full');
            cartOverlay.classList.toggle('hidden');
        }

        function adicionarAoCarrinho(nome, preco) {
            const itemExistente = cart.find(item => item.nome === nome);
            if (itemExistente) {
                itemExistente.quantidade++;
            } else {
                cart.push({ nome, preco, quantidade: 1 });
            }
            renderizarCarrinho();
        }

        function removerDoCarrinho(nome) {
            const itemIndex = cart.findIndex(item => item.nome === nome);
            if (itemIndex > -1) {
                if (cart[itemIndex].quantidade > 1) {
                    cart[itemIndex].quantidade--;
                } else {
                    cart.splice(itemIndex, 1);
                }
            }
            renderizarCarrinho();
        }

        function renderizarCarrinho() {
            cartItemsContainer.innerHTML = '';
            let total = 0;
            let totalItens = 0;

            if (cart.length === 0) {
                cartItemsContainer.innerHTML = '<p class="text-center text-gray-500">Seu carrinho está vazio.</p>';
            } else {
                 cart.forEach(item => {
                    const itemElement = document.createElement('div');
                    itemElement.className = 'flex justify-between items-center mb-4 border-b pb-2';
                    itemElement.innerHTML = `
                        <div>
                            <p class="font-bold">${item.nome}</p>
                            <p class="text-sm text-stone-600">R$ ${item.preco.toFixed(2).replace('.', ',')}</p>
                        </div>
                        <div class="flex items-center cart-item-controls">
                            <button class="bg-gray-200 rounded-full font-bold" onclick="removerDoCarrinho('${item.nome}')">-</button>
                            <span class="mx-2">${item.quantidade}</span>
                            <button class="bg-gray-200 rounded-full font-bold" onclick="adicionarAoCarrinho('${item.nome}', ${item.preco})">+</button>
                        </div>
                    `;
                    cartItemsContainer.appendChild(itemElement);
                    total += item.preco * item.quantidade;
                });
            }
            
            totalItens = cart.reduce((acc, item) => acc + item.quantidade, 0);

            cartTotalElement.innerText = `R$ ${total.toFixed(2).replace('.', ',')}`;
            
            if (totalItens > 0) {
                cartCounterElement.innerText = totalItens;
                cartCounterElement.classList.remove('hidden');
            } else {
                cartCounterElement.classList.add('hidden');
            }
        }

        function finalizarPedido() {
            if (cart.length === 0) {
                alert('Seu carrinho está vazio!');
                return;
            }

            const numeroWhatsApp = '5511999999999'; // 🔥 SUBSTITUA PELO SEU NÚMERO
            let mensagem = 'Olá, JKL Lanches! Gostaria de fazer o seguinte pedido:\n\n';
            let total = 0;

            cart.forEach(item => {
                mensagem += `${item.quantidade}x ${item.nome} - R$ ${(item.preco * item.quantidade).toFixed(2).replace('.', ',')}\n`;
                total += item.preco * item.quantidade;
            });

            mensagem += `\n*Total: R$ ${total.toFixed(2).replace('.', ',')}*`;

            const link = `https://wa.me/${numeroWhatsApp}?text=${encodeURIComponent(mensagem)}`;
            window.open(link, '_blank');
        }

        cartButton.addEventListener('click', toggleCart);
        closeCartButton.addEventListener('click', toggleCart);
        cartOverlay.addEventListener('click', toggleCart);
        finalizeOrderButton.addEventListener('click', finalizarPedido);

        // Disponibiliza as funções globalmente para serem chamadas pelo HTML
        window.adicionarAoCarrinho = adicionarAoCarrinho;
        window.removerDoCarrinho = removerDoCarrinho;

    </script>
</body>
</html>

