        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
            background: linear-gradient(135deg, #1a0033 0%, #330066 50%, #6600cc 100%); 
            min-height: 100vh; 
            color: white; 
            overflow-x: hidden;
        }
        .header { 
            text-align: center; padding: 30px 20px; 
            background: linear-gradient(45deg, #ff1493, #ff69b4, #ff1493); 
            box-shadow: 0 10px 30px rgba(255,20,147,0.4);
            margin-bottom: 30px;
        }
        .header h1 { 
            font-size: 2.5em; margin-bottom: 10px; 
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5); 
            background: linear-gradient(45deg, #fff, #ffd700); 
            -webkit-background-clip: text; 
            -webkit-text-fill-color: transparent; 
        }
        .header p { font-size: 1.2em; opacity: 0.9; }
        .stats { 
            display: flex; justify-content: space-around; flex-wrap: wrap; gap: 20px; 
            background: rgba(255,255,255,0.1); backdrop-filter: blur(10px); 
            padding: 20px; border-radius: 20px; margin-bottom: 30px; 
            box-shadow: 0 8px 32px rgba(0,0,0,0.3);
        }
        .stat { text-align: center; font-weight: bold; font-size: 1.2em; }
        .checkin { text-align: center; margin: 30px 0; }
        button { 
            background: linear-gradient(45deg, #ff1493, #ff69b4); 
            color: white; border: none; padding: 15px 30px; 
            border-radius: 50px; font-size: 18px; font-weight: bold; 
            cursor: pointer; transition: all 0.3s ease; 
            box-shadow: 0 5px 15px rgba(255,20,147,0.4);
            margin: 0 10px;
        }
        button:hover:not(:disabled) { transform: translateY(-3px); box-shadow: 0 8px 25px rgba(255,20,147,0.6); }
        button:disabled { background: #666; cursor: not-allowed; transform: none; box-shadow: none; }
        .album { 
            display: grid; 
            grid-template-columns: repeat(5, 1fr); 
            gap: 20px; max-width: 1000px; margin: 0 auto; padding: 0 20px; 
        }
        .card { 
            aspect-ratio: 2/3; border-radius: 20px; 
            display: flex; flex-direction: column; align-items: center; 
            justify-content: center; position: relative; overflow: hidden;
            transition: all 0.4s ease; cursor: pointer;
        }
        .card.vacia { 
            background: linear-gradient(135deg, rgba(255,255,255,0.1), rgba(255,255,255,0.05)); 
            border: 3px dashed rgba(255,255,255,0.3); backdrop-filter: blur(5px);
        }
        .card.vacia::before { content: '🎴'; font-size: 3em; opacity: 0.5; }
        .card.llenada { 
            background: linear-gradient(135deg, rgba(255,215,0,0.2), rgba(255,20,147,0.2)); 
            border: 3px solid; border-image: linear-gradient(45deg, #ffd700, #ff1493) 1;
            box-shadow: 0 15px 40px rgba(255,20,147,0.4); transform: scale(1.05);
        }
        .card img { 
            width: 100%; height: 100%; object-fit: cover; border-radius: 17px; 
            transition: transform 0.3s ease;
        }
        .card.llenada:hover img { transform: scale(1.1); }
        .progreso { text-align: center; margin-top: 30px; font-size: 1.5em; font-weight: bold; }
        @media (max-width: 768px) { 
            .album { grid-template-columns: repeat(3, 1fr); gap: 15px; } 
            .header h1 { font-size: 2em; }
            .stats { flex-direction: column; gap: 10px; }
        }
