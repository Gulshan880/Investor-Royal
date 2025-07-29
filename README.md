# Investor-Royal 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Royal Game Platform - Play & Win Real Money!</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #ff5722;
            --secondary: #ff9800;
            --dark: #1a1a2e;
            --darker: #16213e;
            --light: #e6e6e6;
            --success: #4CAF50;
            --danger: #f44336;
            --info: #2196F3;
            --gold: #FFD700;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, var(--darker), var(--dark));
            color: var(--light);
            min-height: 100vh;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background: rgba(26, 26, 46, 0.9);
            backdrop-filter: blur(10px);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo h1 {
            font-size: 24px;
            background: linear-gradient(to right, var(--secondary), var(--primary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 700;
        }
        
        .user-info {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .balance {
            background: rgba(255, 152, 0, 0.2);
            padding: 8px 15px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            gap: 8px;
            font-weight: 600;
        }
        
        .balance i {
            color: var(--gold);
        }
        
        .profile {
            display: flex;
            align-items: center;
            gap: 8px;
            background: rgba(255, 255, 255, 0.1);
            padding: 5px 15px;
            border-radius: 20px;
            cursor: pointer;
        }
        
        .profile img {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            object-fit: cover;
        }
        
        /* Main Content */
        .main-content {
            display: flex;
            gap: 20px;
            padding: 30px 0;
        }
        
        /* Sidebar */
        .sidebar {
            width: 250px;
            background: rgba(26, 26, 46, 0.7);
            border-radius: 15px;
            padding: 20px;
            height: fit-content;
        }
        
        .sidebar-menu {
            list-style: none;
        }
        
        .sidebar-menu li {
            margin-bottom: 10px;
        }
        
        .sidebar-menu a {
            display: flex;
            align-items: center;
            gap: 12px;
            padding: 12px 15px;
            border-radius: 10px;
            text-decoration: none;
            color: var(--light);
            transition: all 0.3s;
        }
        
        .sidebar-menu a:hover, .sidebar-menu a.active {
            background: var(--primary);
            transform: translateX(5px);
        }
        
        .sidebar-menu i {
            width: 20px;
            text-align: center;
        }
        
        /* Game Content */
        .game-content {
            flex: 1;
        }
        
        .section-title {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 20px;
        }
        
        .section-title h2 {
            font-size: 24px;
            position: relative;
            padding-left: 15px;
        }
        
        .section-title h2::before {
            content: '';
            position: absolute;
            left: 0;
            top: 5px;
            height: 20px;
            width: 5px;
            background: var(--primary);
            border-radius: 10px;
        }
        
        /* Games Grid */
        .games-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }
        
        .game-card {
            background: rgba(26, 26, 46, 0.7);
            border-radius: 15px;
            overflow: hidden;
            transition: all 0.3s;
            position: relative;
            cursor: pointer;
        }
        
        .game-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }
        
        .game-card img {
            width: 100%;
            height: 140px;
            object-fit: cover;
        }
        
        .game-info {
            padding: 15px;
        }
        
        .game-info h3 {
            font-size: 16px;
            margin-bottom: 5px;
        }
        
        .game-stats {
            display: flex;
            justify-content: space-between;
            font-size: 12px;
            color: #aaa;
        }
        
        .popular-games {
            margin-bottom: 40px;
        }
        
        /* Featured Game */
        .featured-game {
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            border-radius: 20px;
            overflow: hidden;
            margin-bottom: 40px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .featured-content {
            display: flex;
            height: 300px;
        }
        
        .featured-info {
            flex: 1;
            padding: 30px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        .featured-info h2 {
            font-size: 32px;
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        .featured-info p {
            margin-bottom: 20px;
            line-height: 1.6;
        }
        
        .featured-image {
            flex: 1;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), 
                        url('https://images.unsplash.com/photo-1610890716171-6b1bb98ffd09?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80') center/cover;
        }
        
        /* Buttons */
        .btn {
            display: inline-block;
            padding: 12px 25px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            border: none;
            font-size: 16px;
        }
        
        .btn-primary {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(255, 87, 34, 0.4);
        }
        
        .btn-secondary {
            background: rgba(255, 255, 255, 0.1);
            color: white;
        }
        
        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.2);
        }
        
        /* Wallet Section */
        .wallet-section {
            background: rgba(26, 26, 46, 0.7);
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 30px;
        }
        
        .wallet-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .wallet-actions {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-bottom: 25px;
        }
        
        .wallet-action {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s;
            cursor: pointer;
        }
        
        .wallet-action:hover {
            background: rgba(255, 87, 34, 0.2);
            transform: translateY(-3px);
        }
        
        .wallet-action i {
            font-size: 28px;
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        /* Games List */
        .games-list {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }
        
        .game-tag {
            background: rgba(255, 255, 255, 0.1);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 14px;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .game-tag:hover {
            background: var(--primary);
        }
        
        /* Footer */
        footer {
            background: rgba(10, 10, 20, 0.9);
            padding: 40px 0 20px;
            margin-top: 50px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-column h3 {
            font-size: 18px;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 3px;
            background: var(--primary);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 12px;
        }
        
        .footer-column ul li a {
            color: #aaa;
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: var(--primary);
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 15px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #777;
            font-size: 14px;
        }
        
        /* Responsive */
        @media (max-width: 900px) {
            .featured-content {
                flex-direction: column;
                height: auto;
            }
            
            .footer-content {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            .sidebar {
                width: 100%;
            }
            
            .wallet-actions {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
        @media (max-width: 480px) {
            .header-container {
                flex-direction: column;
                gap: 15px;
            }
            
            .games-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .wallet-actions {
                grid-template-columns: 1fr;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
            }
        }
        
        /* Animations */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        .floating {
            animation: float 3s ease-in-out infinite;
        }
        
        /* Badges */
        .badge {
            display: inline-block;
            padding: 3px 8px;
            border-radius: 10px;
            font-size: 12px;
            font-weight: bold;
        }
        
        .badge-hot {
            background: var(--danger);
        }
        
        .badge-new {
            background: var(--success);
        }
        
        .badge-offer {
            background: var(--info);
        }
        
        /* Game Modal */
        .game-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1000;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s;
        }
        
        .game-modal.active {
            opacity: 1;
            visibility: visible;
        }
        
        .modal-content {
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            border-radius: 20px;
            width: 90%;
            max-width: 800px;
            padding: 30px;
            position: relative;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5);
        }
        
        .close-modal {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 24px;
            cursor: pointer;
            color: white;
            background: var(--danger);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .game-container {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .game-header {
            text-align: center;
            margin-bottom: 20px;
        }
        
        .game-header h2 {
            font-size: 32px;
            color: var(--gold);
            margin-bottom: 10px;
        }
        
        .game-area {
            display: flex;
            justify-content: space-between;
            gap: 20px;
        }
        
        .game-board {
            flex: 1;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 20px;
            min-height: 300px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        
        .game-controls {
            width: 250px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 20px;
        }
        
        .bet-controls {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }
        
        .bet-btn {
            flex: 1;
            min-width: 80px;
            padding: 10px;
            background: rgba(255, 255, 255, 0.1);
            border: none;
            border-radius: 10px;
            color: white;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .bet-btn:hover {
            background: rgba(255, 87, 34, 0.3);
        }
        
        .bet-btn.active {
            background: var(--primary);
        }
        
        .play-btn {
            width: 100%;
            padding: 15px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            border: none;
            border-radius: 10px;
            color: white;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
            margin-top: 10px;
        }
        
        .play-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(255, 87, 34, 0.4);
        }
        
        .dice-container {
            display: flex;
            gap: 20px;
            margin: 30px 0;
        }
        
        .dice {
            width: 80px;
            height: 80px;
            background: white;
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 40px;
            font-weight: bold;
            color: var(--dark);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .result-display {
            font-size: 24px;
            font-weight: bold;
            text-align: center;
            min-height: 40px;
            margin: 20px 0;
            color: var(--gold);
        }
        
        .win-animation {
            animation: win 1s ease-in-out;
        }
        
        @keyframes win {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <i class="fas fa-crown fa-2x" style="color: var(--gold);"></i>
                <h1>Royal Game Platform</h1>
            </div>
            <div class="user-info">
                <div class="balance">
                    <i class="fas fa-wallet"></i>
                    ₹ <span id="user-balance">12,456</span>
                </div>
                <div class="profile">
                    <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="User">
                    <span>Rajesh K.</span>
                </div>
            </div>
        </div>
    </header>
    
    <!-- Main Content -->
    <div class="container main-content">
        <!-- Sidebar -->
        <aside class="sidebar">
            <ul class="sidebar-menu">
                <li><a href="#" class="active"><i class="fas fa-home"></i> Dashboard</a></li>
                <li><a href="#"><i class="fas fa-gamepad"></i> All Games</a></li>
                <li><a href="#"><i class="fas fa-wallet"></i> My Wallet</a></li>
                <li><a href="#"><i class="fas fa-gift"></i> Bonuses</a></li>
                <li><a href="#"><i class="fas fa-users"></i> Refer & Earn</a></li>
                <li><a href="#"><i class="fas fa-trophy"></i> Tournaments</a></li>
                <li><a href="#"><i class="fas fa-history"></i> History</a></li>
                <li><a href="#"><i class="fas fa-percentage"></i> Commission</a></li>
                <li><a href="#"><i class="fas fa-cog"></i> Settings</a></li>
                <li><a href="#"><i class="fas fa-headset"></i> Support</a></li>
            </ul>
        </aside>
        
        <!-- Game Content -->
        <main class="game-content">
            <!-- Featured Game -->
            <section class="featured-game">
                <div class="featured-content">
                    <div class="featured-info">
                        <h2>Teen Patti <span class="badge badge-hot">HOT</sp
