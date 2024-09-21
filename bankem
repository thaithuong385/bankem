<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dino's cream</title>
    <style>
        /* Các kiểu dáng đã được giữ nguyên */
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
        }
        .container {
            border: black 10px solid;
            width: 90%;
            margin: 20px auto;
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        header {
            border-bottom: solid 1px red;
            background-color: lightcoral;
            padding: 20px 0;
            position: relative;
        }
        header h1 {
            margin: 0;
            font-size: 2.5em;
            color: white;
            text-align: center;
        }
        nav {
            margin: 10px 0;
            background-color: lightblue;
            padding: 10px 0;
        }
        nav ul {
            list-style-type: none;
            padding: 0;
            margin: 0;
            text-align: center;
        }
        nav li {
            display: inline-block;
            border: solid 2px red;
            background-color: aqua;
            padding: 10px 20px;
            margin: 0 5px;
            transition: background-color 0.3s;
            cursor: pointer;
        }
        nav li:hover {
            background-color: #7fffd4;
        }
        .login-register {
            position: absolute;
            right: 20px;
            top: 20px;
        }
        .login-register a {
            margin: 0 10px;
            color: white;
            text-decoration: none;
            cursor: pointer;
        }
        .tab-container {
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 20px 0;
        }
        .arrow {
            background-color: lightcoral;
            border: none;
            color: white;
            padding: 10px 15px;
            cursor: pointer;
            font-size: 20px;
            transition: background-color 0.3s;
        }
        .arrow:disabled {
            background-color: grey;
            cursor: not-allowed;
        }
        .arrow:hover:not(:disabled) {
            background-color: #c41a27;
        }
        .tab {
            display: inline-block;
            border: solid 2px red;
            background-color: aqua;
            padding: 10px 20px;
            margin: 0 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .tab:hover {
            background-color: #7fffd4;
        }
        section {
            padding: 20px;
            border-bottom: solid 1px #ddd;
        }
        section h2 {
            margin-top: 0;
        }
        .product-grid {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }
        .product {
            border: solid 1px lightgreen;
            padding: 10px;
            margin: 10px;
            background-color: #e0ffe0;
            text-align: left;
            width: calc(33.33% - 20px);
            box-sizing: border-box;
        }
        .product img {
            width: 100px;
            height: auto;
            border-radius: 8px;
            margin-right: 15px;
        }
        footer {
            text-align: center;
            padding: 15px;
            border-top: solid 1px red;
            background-color: lightcoral;
            color: white;
        }
        .hidden {
            display: none;
        }
        .cart-items {
            margin-top: 20px;
            border-top: solid 1px #ddd;
            padding-top: 10px;
        }
        .remove-button {
            background-color: red;
            color: white;
            border: none;
            padding: 5px 10px;
            cursor: pointer;
            margin-left: 10px;
        }
        /* Định dạng modal */
        .modal {
            display: none; 
            position: fixed; 
            z-index: 1; 
            left: 0;
            top: 0;
            width: 100%; 
            height: 100%; 
            overflow: auto; 
            background-color: rgb(0,0,0); 
            background-color: rgba(0,0,0,0.4); 
            padding-top: 60px; 
        }
        .modal-content {
            background-color: #fefefe;
            margin: 5% auto; 
            padding: 20px;
            border: 1px solid #888;
            width: 300px; 
            border-radius: 8px;
        }
        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
        }
        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
        .input-group {
            margin-bottom: 15px;
        }
        .input-group label {
            display: block;
            margin-bottom: 5px;
        }
        .input-group input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-sizing: border-box;
        }
        .login-button, .register-button {
            width: 100%;
            padding: 10px;
            background-color: #e71d2b; /* Màu đỏ giống Thế Giới Di Động */
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }
        .login-button:hover, .register-button:hover {
            background-color: #c41a27;
        }
        .notification {
            margin: 20px 0;
            padding: 10px;
            background-color: #d4edda;
            color: #155724;
            border: 1px solid #c3e6cb;
            border-radius: 5px;
            display: none; /* Hidden by default */
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>DINO'S CREAM</h1>
            <div class="login-register">
                <span id="userNameDisplay" style="color: white;"></span>
                <a href="javascript:void(0);" id="loginBtn">Đăng Nhập</a>
                <a href="javascript:void(0);" id="registerBtn">Đăng Ký</a>
                <a href="javascript:void(0);" id="logoutBtn" class="hidden">Đăng Xuất</a>
            </div>
            <nav>
                <ul>
                    <h2>Sale</h2>
                </ul>
            </nav>
        </header>

        <section id="products">
            <div id="page1" class="product-grid">
                <div class="product">
                    <img src="vanilla.jpg" alt="Kem Vanila">
                    <h3>Kem Vanila</h3>
                    <p>Giá: 25,000 VND</p>
                    <button onclick="addToCart('Kem Vanila', '25,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="chocolate.jpg" alt="Kem Socola">
                    <h3>Kem Socola</h3>
                    <p>Giá: 30,000 VND</p>
                    <button onclick="addToCart('Kem Socola', '30,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="KemDau.jpg" alt="Kem Dâu">
                    <h3>Kem Dâu</h3>
                    <p>Giá: 28,000 VND</p>
                    <button onclick="addToCart('Kem Dâu', '28,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="matcha.jpg" alt="Kem Matcha">
                    <h3>Kem Matcha</h3>
                    <p>Giá: 35,000 VND</p>
                    <button onclick="addToCart('Kem Matcha', '35,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="mango.jpg" alt="Kem Xoài">
                    <h3>Kem Xoài</h3>
                    <p>Giá: 32,000 VND</p>
                    <button onclick="addToCart('Kem Xoài', '32,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="strawberry.jpg" alt="Kem Sầu Riêng">
                    <h3>Kem Sầu Riêng</h3>
                    <p>Giá: 30,000 VND</p>
                    <button onclick="addToCart('Kem Dâu Tây', '30,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="cherry.jpg" alt="Kem Anh Đào">
                    <h3>Kem Anh Đào</h3>
                    <p>Giá: 30,000 VND</p>
                    <button onclick="addToCart('Kem Anh Đào', '30,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="pistachio.jpg" alt="Kem Bột Phỉ">
                    <h3>Kem Bột Phỉ</h3>
                    <p>Giá: 38,000 VND</p>
                    <button onclick="addToCart('Kem Bột Phỉ', '38,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="lemon.jpg" alt="Kem Chanh">
                    <h3>Kem Chanh</h3>
                    <p>Giá: 30,000 VND</p>
                    <button onclick="addToCart('Kem Chanh', '30,000 VND')">Thêm vào Giỏ</button>
                </div>
            </div>
            <div id="page2" class="product-grid hidden">
                <div class="product">
                    <img src="coconut.jpg" alt="Kem Dừa">
                    <h3>Kem Dừa</h3>
                    <p>Giá: 30,000 VND</p>
                    <button onclick="addToCart('Kem Dừa', '30,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="blueberry.jpg" alt="Kem Việt Quất">
                    <h3>Kem Việt Quất</h3>
                    <p>Giá: 35,000 VND</p>
                    <button onclick="addToCart('Kem Việt Quất', '35,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="raspberry.jpg" alt="Kem Mâm Xôi">
                    <h3>Kem Mâm Xôi</h3>
                    <p>Giá: 32,000 VND</p>
                    <button onclick="addToCart('Kem Mâm Xôi', '32,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="toffee.jpg" alt="Kem Kẹo Bơ">
                    <h3>Kem Kẹo Bơ</h3>
                    <p>Giá: 38,000 VND</p>
                    <button onclick="addToCart('Kem Kẹo Bơ', '38,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="peach.jpg" alt="Kem Đào">
                    <h3>Kem Đào</h3>
                    <p>Giá: 30,000 VND</p>
                    <button onclick="addToCart('Kem Đào', '30,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="cookies.jpg" alt="Kem Bánh Quy">
                    <h3>Kem Bánh Quy</h3>
                    <p>Giá: 33,000 VND</p>
                    <button onclick="addToCart('Kem Bánh Quy', '33,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="caramel.jpg" alt="Kem Caramel">
                    <h3>Kem Caramel</h3>
                    <p>Giá: 37,000 VND</p>
                    <button onclick="addToCart('Kem Caramel', '37,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="passionfruit.jpg" alt="Kem Chanh Leo">
                    <h3>Kem Chanh Leo</h3>
                    <p>Giá: 34,000 VND</p>
                    <button onclick="addToCart('Kem Chanh Leo', '34,000 VND')">Thêm vào Giỏ</button>
                </div>
                <div class="product">
                    <img src="taro.jpg" alt="Kem Khoai Môn">
                    <h3>Kem Khoai Môn</h3>
                    <p>Giá: 36,000 VND</p>
                    <button onclick="addToCart('Kem Khoai Môn', '36,000 VND')">Thêm vào Giỏ</button>
                </div>
            </div>
            <div class="tab-container">
                <button class="arrow" id="prevPage" onclick="changePage(-1)">❮</button>
                <div class="tab" id="tabPage">1</div>
                <button class="arrow" id="nextPage" onclick="changePage(1)">❯</button>
            </div>
            <div class="cart-items" id="cartItems">
                <h2>Giỏ Hàng</h2>
                <div id="cartContent"></div>
                <button id="checkoutBtn">Thanh Toán</button>
            </div>
        </section>
    </div>
    <footer>
        <p>Bản quyền © 2024 Dino's Cream</p>
    </footer>

    <!-- Modal Đăng Nhập -->
    <div id="loginModal" class="modal">
        <div class="modal-content">
            <span class="close" id="closeLoginModal">&times;</span>
            <h2>Đăng Nhập</h2>
            <div class="input-group">
                <label for="username">Tên Đăng Nhập</label>
                <input type="text" id="username" placeholder="Nhập tên đăng nhập">
            </div>
            <div class="input-group">
                <label for="password">Mật Khẩu</label>
                <input type="password" id="password" placeholder="Nhập mật khẩu">
            </div>
            <button class="login-button" id="loginSubmit">Đăng Nhập</button>
        </div>
    </div>

    <!-- Modal Đăng Ký -->
    <div id="registerModal" class="modal">
        <div class="modal-content">
            <span class="close" id="closeRegisterModal">&times;</span>
            <h2>Đăng Ký</h2>
            <div class="input-group">
                <label for="newUsername">Tên Đăng Ký</label>
                <input type="text" id="newUsername" placeholder="Nhập tên đăng ký">
            </div>
            <div class="input-group">
                <label for="newPassword">Mật Khẩu</label>
                <input type="password" id="newPassword" placeholder="Nhập mật khẩu">
            </div>
            <button class="register-button" id="registerSubmit">Đăng Ký</button>
        </div>
    </div>

    <script>
        let currentPage = 1; // Biến lưu trang hiện tại
        const totalPages = 2; // Tổng số trang

        // Chức năng chuyển trang
        function changePage(direction) {
            document.getElementById(page${currentPage}).classList.add('hidden');
            currentPage += direction;
            if (currentPage < 1) {
                currentPage = 1;
            } else if (currentPage > totalPages) {
                currentPage = totalPages;
            }
            document.getElementById(page${currentPage}).classList.remove('hidden');
            document.getElementById('tabPage').innerText =  ${currentPage};
            document.getElementById('prevPage').disabled = currentPage === 1;
            document.getElementById('nextPage').disabled = currentPage === totalPages;
        }

        // Chức năng thêm sản phẩm vào giỏ hàng
        const cart = [];

        function addToCart(productName, productPrice) {
            cart.push({ name: productName, price: productPrice });
            displayCart();
        }

        function displayCart() {
            const cartContent = document.getElementById('cartContent');
            cartContent.innerHTML = '';
            cart.forEach((item, index) => {
                cartContent.innerHTML += <div>${item.name} - ${item.price} <button class="remove-button" onclick="removeFromCart(${index})">Xóa</button></div>;
            });
        }

        function removeFromCart(index) {
            cart.splice(index, 1);
            displayCart();
        }

// Giả lập danh sách tài khoản đã đăng ký
let registeredUsers = [];

// Hàm xử lý đăng ký
document.getElementById("registerSubmit").addEventListener("click", function() {
    const newUsername = document.getElementById("newUsername").value;
    const newPassword = document.getElementById("newPassword").value;

    // Kiểm tra xem tài khoản đã tồn tại chưa
    if (registeredUsers.some(user => user.username === newUsername)) {
        alert("Tài khoản đã tồn tại! Vui lòng chọn tên khác.");
    } else {
        // Thêm tài khoản mới vào danh sách
        registeredUsers.push({ username: newUsername, password: newPassword });
        alert("Đăng ký thành công!");
        document.getElementById("closeRegisterModal").click(); // Đóng modal đăng ký
    }
});

// Hàm xử lý đăng nhập
document.getElementById("loginSubmit").addEventListener("click", function() {
    const username = document.getElementById("username").value;
    const password = document.getElementById("password").value;

    // Kiểm tra tài khoản
    const user = registeredUsers.find(user => user.username === username && user.password === password);
    
    if (user) {
        alert("Đăng nhập thành công!");
        // Thực hiện các hành động sau khi đăng nhập thành công
        document.getElementById("closeLoginModal").click(); // Đóng modal đăng nhập
    } else {
        alert("Tài khoản hoặc mật khẩu không đúng. Vui lòng thử lại.");
    }
});


        
        };
    </script>
</body>
</html>
