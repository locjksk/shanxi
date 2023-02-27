


<!doctype html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8"><base>
<meta name="viewport"
	content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
<meta http-equiv="X-UA-Compatible" content="ie=edge">
<link rel="stylesheet"
	href="http://api.zhitaosoft.com:80/dzzz/static/thirdparty/bootstrap-3.3.7/css/bootstrap.min.css">
<link rel="stylesheet" href="http://api.zhitaosoft.com:80/dzzz/static/search/css/common.css">
<link rel="stylesheet" href="http://api.zhitaosoft.com:80/dzzz/static/search/css/detail.css">
<script src="http://api.zhitaosoft.com:80/dzzz/static/thirdparty/jquery/jquery.js"></script>
<script
	src="http://api.zhitaosoft.com:80/dzzz/static/thirdparty/bootstrap-3.3.7/js/bootstrap.min.js"></script>
<script
	src="http://api.zhitaosoft.com:80/dzzz/static/thirdparty/validateform/Validform.min.js"></script>
<script src="http://api.zhitaosoft.com:80/dzzz/static/thirdparty/layer/layer.js"></script>
<title>证书查询结果</title>
<style type="text/css">
#downloadPDF {
	cursor: pointer;
}

.img-container {
	position: relative;
}

.img-container1 {
	position: relative;
}

.add-img {
	position: absolute;
	bottom: 15%;
	right: 27%;
	width: 22%;
	height: 15%;
}

.add-img1 {
	position: absolute;
	bottom: 6%;
	right: 13%;
	width: 22%;
	height: 15%;
}

.add-img>img {
	width: 100%;
	height: 100%;
}

.add-img1>img {
	width: 100%;
	height: 100%;
}
</style>
</head>
<body>
	<header class="header">
		<h1>
			<img class="logo" src="http://api.zhitaosoft.com:80/dzzz/static/search/img/logo.png">陕西省住建厅综合服务中心
		</h1>
	</header>
	<div class="container" id="statt" style="display:none">
		<h3>证书查询结果</h3>
		<div class="row">
			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-4">姓名：</span> <span class="col-md-8" id="name"></span>
			</p>
			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-4">性别：</span> <span class="col-md-8" id="sex"></span>
		</div>
		<div class="row">
			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-4">有效期至：</span> <span class="col-md-8" id="date"></span>
			</p>
			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-4">证书编号：</span> <span class="col-md-8"
					id="number"></span>
			</p>
		</div>
		<div class="row">
			<div class="img-container col-md-9 col-md-offset-1">
				<img src="" width="100%" alt="" id="img">
				<div class="add-img">
				
					<img  src="http://api.zhitaosoft.com:80/dzzz/static/img/gg.png" />
				</div>
			</div>
		</div>
	</div>
	<div class="container" id="statt1" style="display:none">
		<h3>证书查询结果</h3>
		<div class="row">
			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-4" id="daima_id"></span> <span class="col-md-8"
					id="daima"></span>
			</p>

			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-4" id="faren_id"></span> <span class="col-md-8"
					id="faren"></span>
		</div>

		<div class="row">
			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-4" id="mingcheng_id"></span> <span
					class="col-md-8" id="mingcheng"></span>
			</p>
			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-4" id="gongsi_id"></span> <span class="col-md-8"
					id="gongsi"></span>
		</div>
		<div class="row">
			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-4" id="shijian_id"></span> <span
					class="col-md-8" id="shijian"></span>
			</p>
			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-4" id="yuanjian_id"></span> <span
					class="col-md-8" id="yuanjian"></span>
			</p>
			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-4" id="bianhao_id"></span> <span
					class="col-md-8" id="bianhao"></span>
			</p>
		</div>
		<div class="row">
			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-4" id="jiguan_id"></span> <span class="col-md-8"
					id="jiguan"></span>
			</p>

			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-4" id="zhusuo_id"></span> <span class="col-md-8"
					id="zhusuo"></span>
		</div>

		<div class="row">
			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-3" id="dengji_id"></span> <span class="col-md-9"
					id="dengji"></span>
			</p>
			<p class="col-md-5 col-md-offset-1">
				<span class="col-md-4" id="leixing_id"></span> <span
					class="col-md-8" id="leixing"></span>
			</p>
		</div>
		<div class="row">
			<div class="img-container1 col-md-9 col-md-offset-1">
				<img src="" width="100%" alt="" id="img1">
				<div class="add-img1">
					<img id="zhang" src="http://api.zhitaosoft.com:80/dzzz/static/img/qy.png" />
				</div>
			</div>
		</div>
	</div>
	<script type="text/javascript">
		$(function() {
			var stat = 'C';

			if (stat == "B") {
				document.getElementById("statt1").style.display = "block";

			} else {
				document.getElementById("statt").style.display = "block";
			}
			var dd = '{"A4001":"陕建安B(2020)0004562","A4002":"B证人员","A4003":"单家涛","A4004":"612425198203171557","A4005":"男","A4006":"陕西盛世电力科技有限公司","A4007":"项目经理","A4008":"其他","A4009":"陕西省住房和城乡建设厅","A4010":1588262400000,"A4011":1588262400000,"A4012":1688054400000,"ZP":"https://dianzizhengzhao.oss-cn-beijing.aliyuncs.com/temp/44027669-1593-45A7-ADCD-609663B71C50.jpg","ZSimg":"http://zhujianzhengshu.oss-cn-beijing.aliyuncs.com/a040/612425198203171557/img/e1abf0a2a37043849e988a0eb0457c38.jpg","ZSpdf":"https://img.zhengshu.zhitaosoft.com/a040/612425198203171557/pdf/8b843ba370344914952d6068f5a89554.pdf","a0100":"df34b116-6978-464d-ac09-bda1e377a9f7","enabled":"1","endStatus":"0","userid":"f5f8cb5a11b64cfd8495ce1474fcf60a"}';
			var json = JSON.parse(dd.replace(/[\t\r\n]/g,""));
			var type = 'C004';
			var url = json["ZP"];
			document.getElementById("img1").src = url;
			if (json["enabled"] != 0) {
				$("#img").attr("src", json["ZSimg"]);
			} else if (json["enabled"] == 0) {
				layer.msg("证书失效!")
			}

			switch (type) {
			case "C001":
				$("#name").text(json["A0101"]);
				if (typeof (json["A0106"]) == "undefined") {
					$("#sex").text("暂无");
				} else {
					$("#sex").text(json["A0106"]);
				}
				$("#date").text(dateFormat(json["A0126"], "Y年m月d日"));
				$("#number").text(json["A0121"]);
				break;
			case "C002":
				$("#name").text(json["A2001"]);
				if (typeof (json["A2012"]) == "undefined") {
					$("#sex").text("暂无");
				} else {
					$("#sex").text(json["A2012"]);
				}
				$("#date").text(dateFormat(json["A2009"], "Y年m月d日"));
				$("#number").text(json["A2007"]);
				break;
			case "C003":
				$("#name").text(json["A3001"]);
				if (typeof (json["A3012"]) == "undefined") {
					$("#sex").text("暂无");
				} else {
					$("#sex").text(json["A3012"]);
				}
				$("#date").text(dateFormat(json["A3009"], "Y年m月d日"));
				$("#number").text(json["A3007"]);
				break;
			case "C004":
				$("#name").text(json["A4003"]);
				if (typeof (json["A4005"]) == "undefined") {
					$("#sex").text("暂无");
				} else {
					$("#sex").text(json["A4005"]);
				}
				$("#date").text(dateFormat(json["A4012"], "Y年m月d日"));
				$("#number").text(json["A4001"]);
				break;
			case "C005":
				$("#name").text(json["A5001"]);
				if (typeof (json["A5013"]) == "undefined") {
					$("#sex").text("暂无");
				} else {
					$("#sex").text(json["A5013"]);
				}
				$("#date").text(dateFormat(json["A5010"], "Y年m月d日"));
				$("#number").text(json["A5006"]);
				break;
			case "C006":
				$("#name").text(json["A6008"]);
				if (typeof (json["A6009"]) == "undefined") {
					$("#sex").text("暂无");
				} else {
					$("#sex").text(json["A6009"]);
				}
				$("#date").text(dateFormat(json["A6005"], "Y年m月d日"));
				$("#number").text(json["A6001"]);
				break;
			case "C007":
				$("#name").text(json["A0101"]);
				if (typeof (json["A0106"]) == "undefined") {
					$("#sex").text("暂无");
				} else {
					$("#sex").text(json["A0106"]);
				}
				$("#date").text(dateFormat(json["A0126"], "Y年m月d日"));
				$("#number").text(json["A0121"]);
				break;
			case "C008":
				$("#name").text(json["A8001"]);
				/* if (typeof (json["A0106"]) == "undefined") { */
					$("#sex").text("暂无");
				/* } else {
					$("#sex").text(json["A0106"]);
				} */
				$("#date").text(dateFormat(json["A8007"], "Y年m月d日"));
				$("#number").text(json["A8003"]);
				break;
			case "B001":
				document.getElementById("mingcheng_id").innerText = "名称：";
				document.getElementById("shijian_id").innerText = "有效期截止：";
				document.getElementById("gongsi_id").innerText = "所在公司：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "法定代表人：";
				document.getElementById("leixing_id").innerText = "公司类型：";
				document.getElementById("zhusuo_id").innerText = "住所：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("dengji_id").innerText = "资质等级：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				$("#mingcheng").text(json["D0102"]);
				if (typeof (json["D0102"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D0102"]);
				}
				$("#shijian").text(dateFormat(json["D0110"], "Y年m月d日"));
				$("#bianhao").text(json["D0107"]);
				$("#faren").text(json["D0104"]);
				$("#leixing").text(json["D0105"]);
				$("#zhusuo").text(json["D0103"]);
				$("#daima").text(json["D0101"]);
				if (typeof (json["D0106"]) != "undefined") {
					var strs = json["D0106"].split(/~/g);
					var html = "";
					for (i = 0; i < strs.length; i++) {
						html = html + strs[i] + "<br/>"; //分割后的字符输出
					}
					$("#dengji").append(html);
				} else {
					$("#dengji").text(json["D0106"].replace(/~/g, " "));
				}
				
				$("#jiguan").text(json["D0108"]);

				break;
			case "B002":
				$("#mingcheng").text(json["D0202"]);
				document.getElementById("mingcheng_id").innerText = "名称：";
				document.getElementById("shijian_id").innerText = "使用件有效期：";
				document.getElementById("yuanjian_id").innerText = "审批件有效期：";
				document.getElementById("gongsi_id").innerText = "所在公司：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "法定代表人：";
				document.getElementById("leixing_id").innerText = "公司类型：";
				document.getElementById("zhusuo_id").innerText = "住所：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("dengji_id").innerText = "资质等级：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D0202"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D0202"]);
				}
				$("#shijian").text(dateFormat(json["D0210"], "Y年m月d日"));
				$("#bianhao").text(json["D0207"]);
				$("#faren").text(json["D0204"]);
				$("#leixing").text(json["D0205"]);
				if (typeof (json["endTime"]) == "undefined") {
					$("#yuanjian").text("暂无");
				} else {
					$("#yuanjian").text(dateFormat(json["endTime"], "Y年m月d日"));
				}
				/* $("#yuanjian").text(dateFormat(json["endTime"], "Y年m月d日")); */
				$("#zhusuo").text(json["D0203"]);
				$("#daima").text(json["D0201"]);
				if (typeof (json["D0206"]) != "undefined") {
					var strs = json["D0206"].split(/~/g);
					var html = "";
					for (i = 0; i < strs.length; i++) {
						html = html + strs[i] + "<br/>"; //分割后的字符输出
					}
					$("#dengji").append(html);
				} else {
					$("#dengji").text(json["D0206"].replace(/~/g, " "));
				}
				$("#dengji").text(json["D0206"].replace(/~/g, " "));
				$("#jiguan").text(json["D0208"]);
				break;
			case "B003":
				document.getElementById("mingcheng_id").innerText = "机构名称：";
				document.getElementById("shijian_id").innerText = "有效期截止：";
				document.getElementById("gongsi_id").innerText = "备案等级：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "法定代表人：";
				document.getElementById("zhusuo_id").innerText = "住所：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				$("#mingcheng").text(json["D0502"]);
				if (typeof (json["D0505"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D0505"]);
				}
				$("#shijian").text(dateFormat(json["D0507"], "Y年m月d日"));
				$("#bianhao").text(json["D0506"]);
				$("#faren").text(json["D0503"]);
				$("#zhusuo").text(json["D0504"]);
				$("#daima").text(json["D0501"]);
				$("#jiguan").text(json["D0508"]);
				break;
			case "B004":
				$("#mingcheng").text(json["D0602"]);
				document.getElementById("mingcheng_id").innerText = "机构名称：";
				document.getElementById("shijian_id").innerText = "使用件有效期：";
				document.getElementById("yuanjian_id").innerText = "审批件有效期：";
				document.getElementById("gongsi_id").innerText = "备案等级：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "法定代表人：";
				document.getElementById("zhusuo_id").innerText = "住所：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D0605"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D0605"]);
				}
				if (typeof (json["endTime"]) == "undefined") {
					$("#yuanjian").text("暂无");
				} else {
					$("#yuanjian").text(dateFormat(json["endTime"], "Y年m月d日"));
				}
				$("#shijian").text(dateFormat(json["D0607"], "Y年m月d日"));
				
				$("#bianhao").text(json["D0606"]);
				$("#faren").text(json["D0603"]);
				$("#zhusuo").text(json["D0604"]);
				$("#daima").text(json["D0601"]);
				$("#jiguan").text(json["D0608"]);
				break;
			case "B005":
				$("#mingcheng").text(json["D1003"]);
				document.getElementById("mingcheng_id").innerText = "企业名称：";
				document.getElementById("shijian_id").innerText = "有效期截止：";
				document.getElementById("gongsi_id").innerText = "经济性质：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "资质等级：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D1004"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D1004"]);
				}
				$("#shijian").text(dateFormat(json["D1008"], "Y年m月d日"));
				$("#bianhao").text(json["D1002"]);
				if (typeof (json["D1005"]) != "undefined") {
					var strs = json["D1005"].split(/~/g);
					var html = "";
					for (i = 0; i < strs.length; i++) {
						html = html + strs[i] + "<br/>"; //分割后的字符输出
					}
					$("#faren").append(html);
				} else {
					$("#faren").text(json["D1005"].replace(/~/g, " "));
				}
				/* $("#faren").text(json["D1005"].replace(/~/g, " ")); */
				$("#daima").text(json["D1001"]);
				$("#jiguan").text(json["D1006"]);
				break;
			case "B006":
				$("#mingcheng").text(json["D1103"]);
				document.getElementById("mingcheng_id").innerText = "企业名称：";
				document.getElementById("shijian_id").innerText = "使用件有效期：";
				document.getElementById("yuanjian_id").innerText = "审批件有效期：";
				document.getElementById("gongsi_id").innerText = "经济性质：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "资质等级：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D1104"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D1104"]);
				}
				if (typeof (json["endTime"]) == "undefined") {
					$("#yuanjian").text("暂无");
				} else {
					$("#yuanjian").text(dateFormat(json["endTime"], "Y年m月d日"));
				}
				$("#shijian").text(dateFormat(json["D1108"], "Y年m月d日"));
				$("#bianhao").text(json["D1102"]);
				if (typeof (json["D1105"]) != "undefined") {
					var strs = json["D1105"].split(/~/g);
					var html = "";
					for (i = 0; i < strs.length; i++) {
						html = html + strs[i] + "<br/>"; //分割后的字符输出
					}
					$("#faren").append(html);
				} else {
					$("#faren").text(json["D1105"].replace(/~/g, " "));
				}
				/* $("#faren").text(json["D1105"].replace(/~/g, " ")); */
				$("#daima").text(json["D1101"]);
				$("#jiguan").text(json["D1106"]);
				break;
			case "B007":
				$("#mingcheng").text(json["D1503"]);
				document.getElementById("mingcheng_id").innerText = "企业名称：";
				document.getElementById("shijian_id").innerText = "有效期截止：";
				document.getElementById("gongsi_id").innerText = "经济性质：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "资质等级：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D1504"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D1504"]);
				}
				$("#shijian").text(dateFormat(json["D1506"], "Y年m月d日"));
				$("#bianhao").text(json["D1502"]);
				if (typeof (json["D1505"]) != "undefined") {
					var strs = json["D1505"].split(/~/g);
					var html = "";
					for (i = 0; i < strs.length; i++) {
						html = html + strs[i] + "<br/>"; //分割后的字符输出
					}
					$("#faren").append(html);
				} else {
					$("#faren").text(json["D1505"].replace(/~/g, " "));
				}
				/* $("#faren").text(json["D1505"].replace(/~/g, " ")); */
				$("#daima").text(json["D1501"]);
				$("#jiguan").text(json["D1507"]);
				break;
			case "B008":
				$("#mingcheng").text(json["D1603"]);
				document.getElementById("mingcheng_id").innerText = "企业名称：";
				document.getElementById("shijian_id").innerText = "使用件有效期：";
				document.getElementById("yuanjian_id").innerText = "审批件有效期：";
				document.getElementById("gongsi_id").innerText = "经济性质：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "资质等级：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D1604"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D1604"]);
				}
				if (typeof (json["endTime"]) == "undefined") {
					$("#yuanjian").text("暂无");
				} else {
					$("#yuanjian").text(dateFormat(json["endTime"], "Y年m月d日"));
				}
				$("#shijian").text(dateFormat(json["D1606"], "Y年m月d日"));
				$("#bianhao").text(json["D1602"]);
				if (typeof (json["D1605"]) != "undefined") {
					var strs = json["D1605"].split(/~/g);
					var html = "";
					for (i = 0; i < strs.length; i++) {
						html = html + strs[i] + "<br/>"; //分割后的字符输出
					}
					$("#faren").append(html);
				} else {
					$("#faren").text(json["D1605"].replace(/~/g, " "));
				}
				/* $("#faren").text(json["D1605"].replace(/~/g, " ")); */
				$("#daima").text(json["D1601"]);
				$("#jiguan").text(json["D1607"]);
				break;
			case "B009":
				$("#mingcheng").text(json["D2004"]);
				document.getElementById("mingcheng_id").innerText = "机构名称：";
				document.getElementById("shijian_id").innerText = "有效期截止：";
				document.getElementById("leixing_id").innerText = "检测范围：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				/* document.getElementById("faren_id").innerText = "建检字第："; */
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D2005"]) == "undefined") {
					$("#leixing").text("暂无");
				} else {
					$("#leixing").text(json["D2005"].replace(/~/g, " "));
				}
				$("#shijian").text(dateFormat(json["D2006"], "Y年m月d日"));
				$("#bianhao").text(json["D2002"]);
				/* $("#faren").text(json["D2003"]); */
				$("#daima").text(json["D2001"]);
				$("#jiguan").text(json["D2007"]);
				break;
			case "B010":
				$("#mingcheng").text(json["D2104"]);
				document.getElementById("mingcheng_id").innerText = "机构名称：";
				document.getElementById("shijian_id").innerText = "使用件有效期：";
				document.getElementById("yuanjian_id").innerText = "审批件有效期：";
				document.getElementById("leixing_id").innerText = "检测范围：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				/* document.getElementById("faren_id").innerText = "建检字第："; */
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D2105"]) == "undefined") {
					$("#leixing").text("暂无");
				} else {
					$("#leixing").text(json["D2105"].replace(/~/g, " "));
				}
				if (typeof (json["endTime"]) == "undefined") {
					$("#yuanjian").text("暂无");
				} else {
					$("#yuanjian").text(dateFormat(json["endTime"], "Y年m月d日"));
				}
				$("#shijian").text(dateFormat(json["D2106"], "Y年m月d日"));
				$("#bianhao").text(json["D2102"]);
				/* $("#faren").text(json["D2103"]); */
				$("#daima").text(json["D2101"]);
				$("#jiguan").text(json["D2107"]);
				break;
			case "B011":
				$("#mingcheng").text(json["D2504"]);
				document.getElementById("mingcheng_id").innerText = "单位名称：";
				document.getElementById("shijian_id").innerText = "有效期截止：";
				document.getElementById("gongsi_id").innerText = "编号：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "主要负责人：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("zhusuo_id").innerText = "单位地址：";
				document.getElementById("dengji_id").innerText = "经济类型：";
				document.getElementById("leixing_id").innerText = "许可范围：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D2502"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D2502"]);
				}
				$("#shijian").text(dateFormat(json["D2509"], "Y年m月d日"));
				$("#bianhao").text(json["D2502"]);
				$("#faren").text(json["D2505"]);
				$("#daima").text(json["D2501"]);
				$("#jiguan").text(json["D2510"]);
				$("#zhusuo").text(json["D2506"]);
				$("#dengji").text(json["D2507"]);
				$("#leixing").text(json["D2508"].replace(/~/g, " "));
				break;
			case "B012":
				$("#mingcheng").text(json["D2604"]);
				document.getElementById("mingcheng_id").innerText = "单位名称：";
				document.getElementById("shijian_id").innerText = "使用件有效期：";
				document.getElementById("yuanjian_id").innerText = "审批件有效期：";
				document.getElementById("gongsi_id").innerText = "编号：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "主要负责人：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("zhusuo_id").innerText = "单位地址：";
				document.getElementById("dengji_id").innerText = "经济类型：";
				document.getElementById("leixing_id").innerText = "许可范围：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D2602"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D2602"]);
				}
				if (typeof (json["endTime"]) == "undefined") {
					$("#yuanjian").text("暂无");
				} else {
					$("#yuanjian").text(dateFormat(json["endTime"], "Y年m月d日"));
				}
				$("#shijian").text(dateFormat(json["D2609"], "Y年m月d日"));
				$("#bianhao").text(json["D2602"]);
				$("#faren").text(json["D2605"]);
				$("#daima").text(json["D2601"]);
				$("#jiguan").text(json["D2610"]);
				$("#zhusuo").text(json["D2606"]);
				$("#dengji").text(json["D2607"]);
				$("#leixing").text(json["D2608"].replace(/~/g, " "));
				break;
			case "B013":
				$("#mingcheng").text(json["D3002"]);
				document.getElementById("mingcheng_id").innerText = "企业名称：";
				document.getElementById("shijian_id").innerText = "有效期截止：";
				document.getElementById("gongsi_id").innerText = "经济性质：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "法定代表人：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("zhusuo_id").innerText = "详细地址：";
				document.getElementById("dengji_id").innerText = "资质类别及等级：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D3008"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D3008"]);
				}
				$("#shijian").text(dateFormat(json["D3010"], "Y年m月d日"));
				$("#bianhao").text(json["D3005"]);
				$("#faren").text(json["D3007"]);
				$("#daima").text(json["D3001"]);
				$("#jiguan").text(json["D3011"]);
				$("#zhusuo").text(json["D3003"]);
				var ss = json["D3011"];
				console.info("》》"+ss);
				if(ss=="西安市城乡建设委员会"  || ss=="西安市住房和城乡建设局" ){
					document.getElementById("zhang").src="static/img/qy6101.png";
					console.info("1111");
				}else {
					console.info("222");
				}
				
				
				var strs = new Array();
				if (typeof (json["D3006"]) != "undefined") {
					var strs = json["D3006"].split(/~/g);
					var html = "";
					for (i = 0; i < strs.length; i++) {
						html = html + strs[i] + "<br/>"; //分割后的字符输出
					}
					$("#dengji").append(html);
				} else {
					$("#dengji").text(json["D3006"].replace(/~/g, " "));
				}
				break;
			case "B014":
				$("#mingcheng").text(json["D3102"]);
				document.getElementById("mingcheng_id").innerText = "企业名称：";
				document.getElementById("shijian_id").innerText = "使用件有效期：";
				document.getElementById("yuanjian_id").innerText = "审批件有效期：";
				document.getElementById("gongsi_id").innerText = "经济性质：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "法定代表人：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("zhusuo_id").innerText = "详细地址：";
				document.getElementById("dengji_id").innerText = "资质类别及等级：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D3108"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D3108"]);
				}
				if (typeof (json["endTime"]) == "undefined") {
					$("#yuanjian").text("暂无");
				} else {
					$("#yuanjian").text(dateFormat(json["endTime"], "Y年m月d日"));
				}
				$("#shijian").text(dateFormat(json["D3110"], "Y年m月d日"));
				$("#bianhao").text(json["D3105"]);
				$("#faren").text(json["D3107"]);
				$("#daima").text(json["D3101"]);
				$("#jiguan").text(json["D3111"]);
				$("#zhusuo").text(json["D3103"]);
				var ss = json["D3111"];
				if(ss=="西安市城乡建设委员会"  || ss=="西安市住房和城乡建设局"){
					document.getElementById("zhang").src="static/img/qy6101.png";
					console.info("1111");
				}else {
					console.info("222");
				}
				
				var strs = new Array();
				if (typeof (json["D3106"]) != "undefined") {
					var strs = json["D3106"].split(/~/g);
					var html = "";
					for (i = 0; i < strs.length; i++) {
						html = html + strs[i] + "<br/>"; //分割后的字符输出
					}
					$("#dengji").append(html);
				} else {
					$("#dengji").text(json["D3106"].replace(/~/g, " "));
				}
				/* $("#dengji").text(json["D3106"].replace(/~/g, " ")); */
				break;
			case "B015":
				$("#mingcheng").text(json["D3502"]);
				document.getElementById("mingcheng_id").innerText = "企业名称：";
				document.getElementById("shijian_id").innerText = "有效期截止：";
				document.getElementById("gongsi_id").innerText = "经济性质：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "法定代表人：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("zhusuo_id").innerText = "详细地址：";
				document.getElementById("dengji_id").innerText = "资质类别及等级：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D3502"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D3502"]);
				}
				$("#shijian").text(dateFormat(json["D3510"], "Y年m月d日"));
				$("#bianhao").text(json["D3505"]);
				$("#faren").text(json["D3507"]);
				$("#daima").text(json["D3501"]);
				$("#jiguan").text(json["D3511"]);
				$("#zhusuo").text(json["D3503"]);
				if (typeof (json["D3506"]) != "undefined") {
					var strs = json["D3506"].split(/~/g);
					var html = "";
					for (i = 0; i < strs.length; i++) {
						html = html + strs[i] + "<br/>"; //分割后的字符输出
					}
					$("#dengji").append(html);
				} else {
					$("#dengji").text(json["D3506"].replace(/~/g, " "));
				}
				/* $("#dengji").text(json["D3506"].replace(/~/g, " ")); */
				break;
			case "B016":
				$("#mingcheng").text(json["D3602"]);
				document.getElementById("mingcheng_id").innerText = "企业名称：";
				document.getElementById("shijian_id").innerText = "使用件有效期：";
				document.getElementById("yuanjian_id").innerText = "审批件有效期：";
				document.getElementById("gongsi_id").innerText = "经济性质：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "法定代表人：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("zhusuo_id").innerText = "详细地址：";
				document.getElementById("dengji_id").innerText = "资质类别及等级：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D3602"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D3602"]);
				}
				if (typeof (json["endTime"]) == "undefined") {
					$("#yuanjian").text("暂无");
				} else {
					$("#yuanjian").text(dateFormat(json["endTime"], "Y年m月d日"));
				}
				$("#shijian").text(dateFormat(json["D3610"], "Y年m月d日"));
				$("#bianhao").text(json["D3605"]);
				$("#faren").text(json["D3607"]);
				$("#daima").text(json["D3601"]);
				$("#jiguan").text(json["D3611"]);
				$("#zhusuo").text(json["D3603"]);
				if (typeof (json["D3606"]) != "undefined") {
					var strs = json["D3606"].split(/~/g);
					var html = "";
					for (i = 0; i < strs.length; i++) {
						html = html + strs[i] + "<br/>"; //分割后的字符输出
					}
					$("#dengji").append(html);
				} else {
					$("#dengji").text(json["D3606"].replace(/~/g, " "));
				}
				/* $("#dengji").text(json["D3606"].replace(/~/g, " ")); */
				break;
			case "B017":
				$("#mingcheng").text(json["D4002"]);
				document.getElementById("mingcheng_id").innerText = "企业名称：";
				document.getElementById("shijian_id").innerText = "有效期截止：";
				document.getElementById("gongsi_id").innerText = "经济性质：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "法定代表人：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("zhusuo_id").innerText = "详细地址：";
				document.getElementById("dengji_id").innerText = "资质等级：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D4008"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D4008"]);
				}
				
				$("#shijian").text(dateFormat(json["D4010"], "Y年m月d日"));
				$("#bianhao").text(json["D4005"]);
				$("#faren").text(json["D4007"]);
				$("#daima").text(json["D4001"]);
				$("#jiguan").text(json["D4011"]);
				$("#zhusuo").text(json["D4003"]);
				if (typeof (json["D4006"]) != "undefined") {
					var strs = json["D4006"].split(/~/g);
					var html = "";
					for (i = 0; i < strs.length; i++) {
						html = html + strs[i] + "<br/>"; //分割后的字符输出
					}
					$("#dengji").append(html);
				} else {
					$("#dengji").text( json["D4006"].replace(/~/g, " "));
				}
				/* $("#dengji").text(json["D4006"].replace(/~/g, " ")); */
				break;
			case "B018":
				$("#mingcheng").text(json["D4102"]);
				document.getElementById("mingcheng_id").innerText = "企业名称：";
				document.getElementById("shijian_id").innerText = "使用件有效期：";
				document.getElementById("yuanjian_id").innerText = "审批件有效期：";
				document.getElementById("gongsi_id").innerText = "经济性质：";
				document.getElementById("bianhao_id").innerText = "证书编号：";
				document.getElementById("faren_id").innerText = "法定代表人：";
				document.getElementById("daima_id").innerText = "信用代码：";
				document.getElementById("zhusuo_id").innerText = "详细地址：";
				document.getElementById("dengji_id").innerText = "资质等级：";
				document.getElementById("jiguan_id").innerText = "发证机关：";
				if (typeof (json["D4102"]) == "undefined") {
					$("#gongsi").text("暂无");
				} else {
					$("#gongsi").text(json["D4102"]);
				}
				if (typeof (json["endTime"]) == "undefined") {
					$("#yuanjian").text("暂无");
				} else {
					$("#yuanjian").text(dateFormat(json["endTime"], "Y年m月d日"));
				}
				$("#shijian").text(dateFormat(json["D4110"], "Y年m月d日"));
				$("#bianhao").text(json["D4105"]);
				$("#faren").text(json["D4107"]);
				$("#daima").text(json["D4101"]);
				$("#jiguan").text(json["D4111"]);
				$("#zhusuo").text(json["D4103"]);
				if (typeof (json["D4106"]) != "undefined") {
					var strs = json["D4106"].split(/~/g);
					var html = "";
					for (i = 0; i < strs.length; i++) {
						html = html + strs[i] + "<br/>"; //分割后的字符输出
					}
					$("#dengji").append(html);
				} else {
					$("#dengji").text(json["D4106"].replace(/~/g, " "));
				}
				/* $("#dengji").text(json["D4106"].replace(/~/g, " ")); */
				break;
			}
		})

		/*
		 ** 时间戳转换成指定格式日期
		 ** eg. 
		 ** dateFormat(11111111111111, 'Y年m月d日 H时i分')
		 ** → "2322年02月06日 03时45分"
		 */
		var dateFormat = function(timestamp, formats) {
			// formats格式包括
			// 1. Y-m-d
			// 2. Y-m-d H:i:s
			// 3. Y年m月d日
			// 4. Y年m月d日 H时i分
			formats = formats || 'Y-m-d';

			var zero = function(value) {
				if (value < 10) {
					return '0' + value;
				}
				return value;
			};

			var myDate = timestamp ? new Date(timestamp) : new Date();

			var year = myDate.getFullYear();
			var month = zero(myDate.getMonth() + 1);
			var day = zero(myDate.getDate());

			var hour = zero(myDate.getHours());
			var minite = zero(myDate.getMinutes());
			var second = zero(myDate.getSeconds());

			return formats.replace(/Y|m|d|H|i|s/ig, function(matches) {
				return ({
					Y : year,
					m : month,
					d : day,
					H : hour,
					i : minite,
					s : second
				})[matches];
			});
		};
	</script>
</body>
</html>
