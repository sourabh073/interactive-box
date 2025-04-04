<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bundle & Save</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            margin: 0;
            background-color: #f8f9fa;
        }
        .container {
            width: 350px;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0,0,0,0.1);
        }
        .bundle {
            border: 2px solid #ccc;
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 10px;
            cursor: pointer;
        }
        .bundle.selected {
            border-color: green;
            background-color: #e6f7e6;
        }
        .bundle-header {
            display: flex;
            justify-content: space-between;
            font-weight: bold;
        }
        .details {
            display: none;
            margin-top: 10px;
        }
        select {
            width: 100%;
            padding: 5px;
            margin-top: 5px;
        }
        .total {
            font-size: 18px;
            font-weight: bold;
            margin-top: 10px;
            text-align: center;
        }
        .add-to-cart {
            width: 100%;
            padding: 10px;
            background: green;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Bundle & Save</h2>
        
        <div class="bundle" onclick="selectBundle(this, 195, 1)">
            <div class="bundle-header">
                <span>1 Pair</span>
                <span>DKK 195.00</span>
            </div>
            <p>50% OFF</p>
            <div class="details">
                <label>Size:</label>
                <select>
                    <option>S</option>
                    <option>M</option>
                    <option>L</option>
                    <option>XL</option>
                </select>
                <label>Color:</label>
                <select>
                    <option>Red</option>
                    <option>Blue</option>
                    <option>Green</option>
                    <option>Black</option>
                </select>
            </div>
        </div>
        
        <div class="bundle" onclick="selectBundle(this, 345, 2)">
            <div class="bundle-header">
                <span>2 Pair</span>
                <span>DKK 345.00</span>
            </div>
            <p>40% OFF</p>
            <div class="details">
                <label>Size:</label>
                <select>
                    <option>S</option>
                    <option>M</option>
                    <option>L</option>
                    <option>XL</option>
                </select>
                <label>Color:</label>
                <select>
                    <option>Red</option>
                    <option>Blue</option>
                    <option>Green</option>
                    <option>Black</option>
                </select>
            </div>
        </div>
        
        <div class="bundle" onclick="selectBundle(this, 528, 3)">
            <div class="bundle-header">
                <span>3 Pair</span>
                <span>DKK 528.00</span>
            </div>
            <p>60% OFF</p>
            <div class="details">
                <label>Size:</label>
                <select>
                    <option>S</option>
                    <option>M</option>
                    <option>L</option>
                    <option>XL</option>
                </select>
                <label>Color:</label>
                <select>
                    <option>Red</option>
                    <option>Blue</option>
                    <option>Green</option>
                    <option>Black</option>
                </select>
            </div>
        </div>
        
        <div class="total">Total: DKK 0.00</div>
        <button class="add-to-cart">+ Add to Cart</button>
    </div>
    
    <script>
        function selectBundle(bundle, price, count) {
            document.querySelectorAll('.bundle').forEach(el => {
                el.classList.remove('selected');
                el.querySelector('.details').style.display = 'none';
            });
            
            bundle.classList.add('selected');
            bundle.querySelector('.details').style.display = 'block';
            document.querySelector('.total').textContent = `Total: DKK ${price}.00`;
        }
    </script>
</body>
</html>
