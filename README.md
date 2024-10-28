<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>产品展示</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            display: flex;
            flex-direction: column; /* 垂直布局 */
            background-color: #f0f0f0;
            height: 100vh; /* 让页面充满整个视口高度 */
        }
        .sidebar {
            width: 250px;
            background-color: #fff;
            padding: 15px;
            box-shadow: 2px 0 10px rgba(0, 0, 0, 0.1);
            overflow-y: auto;
        }
        .brand, .sub-menu-item {
            cursor: pointer;
            margin: 10px 0;
            padding: 10px;
            border-radius: 5px;
            transition: background 0.3s;
        }
        .brand:hover, .sub-menu-item:hover {
            background-color: #e0e0e0;
        }
        .sub-menu {
            display: none;
            margin-left: 10px;
        }
        .content {
            flex: 1; /* 让内容区填满剩余空间 */
            padding: 20px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        .product {
            background: white;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            padding: 15px;
            text-align: center;
            width: 300px;
        }
        .product img {
            border-radius: 10px;
            width: 100%;
            height: auto;
        }
        .pagination {
            display: flex;
            justify-content: center;
            margin: 20px 0; /* 上下间距 */
        }
        .pagination button {
            margin: 0 10px;
            padding: 5px 10px;
            cursor: pointer;
            background-color: #ff4081;
            color: white;
            border: none;
            border-radius: 5px;
            transition: background 0.3s;
        }
        .pagination button:hover {
            background-color: #e91e63;
        }
		.container {
            display: flex; /* 使用 flexbox */
            height: 100vh; /* 设置高度为视口高度 */
        }
        .left {
            flex: 1; /* 左侧 div 占据可用空间 */
            background-color: #4CAF50; /* 背景颜色 */
            color: white; /* 文字颜色 */
            padding: 20px; /* 内边距 */
        }
        .right {
            flex: 2; /* 右侧 div 占据更大的空间 */
            background-color: #f1f1f1; /* 背景颜色 */
            color: black; /* 文字颜色 */
            padding: 20px; /* 内边距 */
        }
		.sidebar-menu {
		  width: 100px; /* 菜单宽度 */
		  height: 100vh; /* 菜单高度，100%视口高度 */
		  overflow-y: scroll; /* 使用垂直滚动条 */
		  border: 0px solid #ccc; /* 菜单边框 */
		  padding: 1px; /* 菜单内部填充 */
		}
        #pageInfo {
            align-self: center;
            margin: 0 10px;
        }
        @media (max-width: 768px) {
            .sidebar {
                width: 100%;
                box-shadow: none;
            }
            .content {
                padding: 10px;
            }
            .product {
                width: 100%; /* 在手机上全宽 */
            }
        }
    </style>
</head>
<body>

<div class="container">
        <div class="left">
		
		<div class="sidebar-menu">
    <h2>品牌列表</h2>
    <div class="brand" onclick="toggleSubMenu('brandA')">兰蔻</div>
    <div class="sub-menu" id="brandA">
        <div class="sub-menu-item" onclick="showProducts('brandA-series1')">小黑瓶系列</div>
        <div class="sub-menu-item" onclick="showProducts('brandA-series2')">菁纯系列</div>
		<div class="sub-menu-item" onclick="showProducts('brandA-series3')">黑金系列</div>
		<div class="sub-menu-item" onclick="showProducts('brandA-series4')">香水系列</div>
    </div>
    <div class="brand" onclick="toggleSubMenu('brandB')">雅诗兰黛</div>
    <div class="sub-menu" id="brandB">
        <div class="sub-menu-item" onclick="showProducts('brandB-series1')">小棕瓶系列</div>
        <div class="sub-menu-item" onclick="showProducts('brandB-series2')">专研系列</div>
		<div class="sub-menu-item" onclick="showProducts('brandB-series3')">胶原系列</div>
    </div>
    <div class="brand" onclick="toggleSubMenu('brandC')">赫莲娜</div>
    <div class="sub-menu" id="brandC">
        <div class="sub-menu-item" onclick="showProducts('brandC-series1')">系列1</div>
        <div class="sub-menu-item" onclick="showProducts('brandC-series2')">系列2</div>
		<div class="sub-menu-item" onclick="showProducts('brandC-series3')">系列3</div>
    </div>
	 <div class="brand" onclick="toggleSubMenu('brandD')">娇韵诗</div>
    <div class="sub-menu" id="brandD">
        <div class="sub-menu-item" onclick="showProducts('brandC-series1')">系列1</div>
        <div class="sub-menu-item" onclick="showProducts('brandC-series2')">系列2</div>
		<div class="sub-menu-item" onclick="showProducts('brandC-series3')">系列3</div>
    </div>
	 <div class="brand" onclick="toggleSubMenu('brandE')">海蓝之谜</div>
    <div class="sub-menu" id="brandE">
        <div class="sub-menu-item" onclick="showProducts('brandC-series1')">系列1</div>
        <div class="sub-menu-item" onclick="showProducts('brandC-series2')">系列2</div>
		<div class="sub-menu-item" onclick="showProducts('brandC-series3')">系列3</div>
    </div>
	<div class="brand" onclick="toggleSubMenu('brandF')">SK2</div>
    <div class="sub-menu" id="brandF">
        <div class="sub-menu-item" onclick="showProducts('brandC-series1')">系列1</div>
        <div class="sub-menu-item" onclick="showProducts('brandC-series2')">系列2</div>
		<div class="sub-menu-item" onclick="showProducts('brandC-series3')">系列3</div>
    </div>
	<div class="brand" onclick="toggleSubMenu('brandG')">资生堂</div>
    <div class="sub-menu" id="brandG">
        <div class="sub-menu-item" onclick="showProducts('brandC-series1')">系列1</div>
        <div class="sub-menu-item" onclick="showProducts('brandC-series2')">系列2</div>
		<div class="sub-menu-item" onclick="showProducts('brandC-series3')">系列3</div>
    </div>
	<div class="brand" onclick="toggleSubMenu('brandH')">修丽可</div>
    <div class="sub-menu" id="brandH">
        <div class="sub-menu-item" onclick="showProducts('brandC-series1')">系列1</div>
        <div class="sub-menu-item" onclick="showProducts('brandC-series2')">系列2</div>
		<div class="sub-menu-item" onclick="showProducts('brandC-series3')">系列3</div>
    </div>
	<div class="brand" onclick="toggleSubMenu('brandI')">娇兰</div>
    <div class="sub-menu" id="brandI">
        <div class="sub-menu-item" onclick="showProducts('brandC-series1')">系列1</div>
        <div class="sub-menu-item" onclick="showProducts('brandC-series2')">系列2</div>
		<div class="sub-menu-item" onclick="showProducts('brandC-series3')">系列3</div>
    </div>
	
	  </div>
        </div>
        <div class="right">
            
<div class="content" id="productDisplay">
    <div class="product" id="productContainer" style="display: none;"></div>
	</div>

	<div class="pagination" id="paginationControls" style="display:none;">
		<button onclick="changePage(-1)">上一页</button>
		<span id="pageInfo"></span>
		<button onclick="changePage(1)">下一页</button>
	</div>
	<div>
			【美丽循环，绿色未来】  ©Send For 圣峰集团（中国）有限公司
	</div>
        </div>
 </div>




<script>
    let currentPage = 1;
    const productsPerPage = 1; // 每页显示一个产品
    let currentProducts = [];

    function toggleSubMenu(brand) {
        const subMenu = document.getElementById(brand);
        subMenu.style.display = subMenu.style.display === 'block' ? 'none' : 'block';
    }

    function showProducts(series) {
        currentPage = 1; // Reset to first page
        const productContainer = document.getElementById('productContainer');
        productContainer.style.display = 'block'; // 显示产品容器

        if (series === 'brandA-series1') {
            currentProducts = [
                { img: 'https://res.lancome.com.cn/resources/2024/10/14/17289002547395999_460X460.jpg?version=20241015103733773', title: '兰蔻小黑瓶系列-「发光」眼霜', desc: '几批要，价格多少' },
				{ img: 'https://res.lancome.com.cn/resources/2024/10/14/172890023689495_460X460.jpg?version=20241015103733773', title: '兰蔻小黑瓶系列-小黑瓶安瓶精华', desc: '几批要，价格多少' },
				{ img: 'https://res.lancome.com.cn/resources/2024/10/14/17288981841801280_460X460.jpg?version=20241015103733773', title: '兰蔻小黑瓶系列-极光水+极光乳液', desc: '几批要，价格多少' },
                { img: 'https://res.lancome.com.cn/resources/2024/10/14/172889949029969_460X460.jpg?version=20241015103733773', title: '兰蔻小黑瓶系-大眼精华', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandA-series2') {
            currentProducts = [
                { img: 'https://res.lancome.com.cn/resources/2024/10/14/172889954591882_460X460.jpg?version=20241015103733773', title: '兰蔻菁纯系列-菁纯眼霜', desc: '几批要，价格多少' },
				 { img: 'https://res.lancome.com.cn/resources/2024/10/14/17288996387194231_460X460.jpg?version=20241015103733773', title: '兰蔻菁纯系列-菁纯面霜', desc: '几批要，价格多少' },
				  { img: 'https://res.lancome.com.cn/resources/2024/10/14/17288997308449447_460X460.jpg?version=20241015103733773', title: '兰蔻菁纯系列-菁纯精华水', desc: '几批要，价格多少' },
				   { img: 'https://res.lancome.com.cn/resources/2024/8/15/17237137294417842_460X460.jpg?version=20241015103733773', title: '兰蔻菁纯系列-菁纯精华乳液', desc: '几批要，价格多少' },
				    { img: 'https://res.lancome.com.cn/resources/2021/4/15/16184766655732553_460X460.jpg?version=20241015103733773', title: '兰蔻菁纯系列-菁纯润白乳霜', desc: '几批要，价格多少' },
                { img: 'https://res.lancome.com.cn/resources/2024/10/14/1728898455833275_460X460.jpg?version=20241015103733773', title: '兰蔻菁纯系列-菁纯身体霜', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandA-series3') {
            currentProducts = [
                { img: 'https://res.lancome.com.cn/resources/2024/10/14/17288994609693861_460X460.jpg?version=20241015103733773', title: '兰蔻黑金系列-黑金臻宠面霜', desc: '几批要，价格多少' },
				{ img: 'https://res.lancome.com.cn/resources/2024/10/14/17288994044672160_460X460.jpg?version=20241015103733773', title: '兰蔻黑金系列-黑金臻宠精华水', desc: '几批要，价格多少' },
				{ img: 'https://res.lancome.com.cn/resources/2024/10/14/17288983543386537_460X460.jpg?version=20241015103733773', title: '兰蔻黑金系列-黑金臻宠眼霜', desc: '几批要，价格多少' },
				{ img: 'https://res.lancome.com.cn/resources/2024/10/14/17288994373714062_460X460.jpg?version=20241015103733773', title: '兰蔻黑金系列-黑金精华乳', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandA-series4') {
            currentProducts = [
                { img: 'https://res.lancome.com.cn/resources/2024/10/14/17288992967957624_460X460.jpg?version=20241015103733773', title: '兰蔻香水系列-IDÔLE「是我」香水', desc: '几批要，价格多少' },
				{ img: 'https://res.lancome.com.cn/resources/2023/11/14/16999755023784413_460X460.jpg?version=20241015103733773', title: '兰蔻香水系列-奇迹香水', desc: '几批要，价格多少' },
				{ img: 'https://res.lancome.com.cn/resources/2020/9/29/16013608534557721_460X460.jpg?version=20241015103733773', title: '兰蔻香水系列-珍爱香水', desc: '几批要，价格多少' },
				{ img: 'https://res.lancome.com.cn/resources/2023/6/20/16872760509886042_460X460.jpg?version=20241015103733773', title: '兰蔻香水系列-兰蔻殿堂香水', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandB-series1') {
            currentProducts = [
                { img: 'https://www.esteelauder.com.cn/media/export/cms/products/308x424/el_sku_PG5701_308x424_0.jpg?w=3840', title: '雅诗兰黛小棕瓶系列-小棕瓶精华', desc: '几批要，价格多少' },
				{ img: 'https://www.esteelauder.com.cn/media/export/cms/products/308x424/el_sku_PYL501_308x424_0.jpg?w=3840', title: '雅诗兰黛小棕瓶系列-小棕瓶眼霜', desc: '几批要，价格多少' },
				{ img: 'https://www.esteelauder.com.cn/media/export/cms/products/308x424/el_sku_GYYK01_308x424_0.jpg?w=3840', title: '雅诗兰黛小棕瓶系列-全新SOS闪修精华', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandB-series2') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '雅诗兰黛专研系列-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌B系列2-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandB-series3') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌B系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌B系列2-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandC-series1') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列1-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列1-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandC-series2') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandC-series3') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品2', desc: '几批要，价格多少' }
            ];
        }else if (series === 'brandD-series1') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列1-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列1-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandD-series2') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandD-series3') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品2', desc: '几批要，价格多少' }
            ];
        }else if (series === 'brandE-series1') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列1-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列1-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandE-series2') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandE-series3') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品2', desc: '几批要，价格多少' }
            ];
        }else if (series === 'brandF-series1') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列1-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列1-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandF-series2') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandF-series3') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品2', desc: '几批要，价格多少' }
            ];
        }else if (series === 'brandG-series1') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列1-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列1-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandG-series2') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandG-series3') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品2', desc: '几批要，价格多少' }
            ];
        }else if (series === 'brandH-series1') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列1-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列1-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandH-series2') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandH-series3') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品2', desc: '几批要，价格多少' }
            ];
        }else if (series === 'brandI-series1') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列1-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列1-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandI-series2') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品2', desc: '几批要，价格多少' }
            ];
        } else if (series === 'brandI-series3') {
            currentProducts = [
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品1', desc: '几批要，价格多少' },
                { img: 'https://via.placeholder.com/300x200', title: '品牌C系列2-产品2', desc: '几批要，价格多少' }
            ];
        }


        displayProducts();
    }

    function displayProducts() {
        const productContainer = document.getElementById('productContainer');
        productContainer.innerHTML = '';

        const start = (currentPage - 1) * productsPerPage;
        const end = start + productsPerPage;
        const productsToShow = currentProducts.slice(start, end);

        productsToShow.forEach(product => {
            productContainer.innerHTML += `
                <img src="${product.img}" alt="${product.title}">
                <h3>${product.title}</h3>
                <p>${product.desc}</p>
            `;
        });

        updatePaginationControls();
    }

    function updatePaginationControls() {
        const paginationControls = document.getElementById('paginationControls');
        const pageInfo = document.getElementById('pageInfo');

        const totalPages = Math.ceil(currentProducts.length / productsPerPage);
        pageInfo.innerText = `第 ${currentPage} 页 / 共 ${totalPages} 页`;

        paginationControls.style.display = totalPages > 1 ? 'flex' : 'none';
    }

    function changePage(direction) {
        const totalPages = Math.ceil(currentProducts.length / productsPerPage);
        currentPage += direction;

        if (currentPage < 1) currentPage = 1;
        if (currentPage > totalPages) currentPage = totalPages;

        displayProducts();
    }
</script>

</body>
</html>
