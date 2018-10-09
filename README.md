# phpBulidCode
BulidCode
# Code 39 Barcode generator

简单的PHP类，用于生成代码39的条形码图像。非常简单的事情

	barcode::code39('text to encode');
可选地，在像素和/或宽度乘法器中添加高度。:

	barcode::code39('text to encode', $height_in_px, $width_multiplier);
	barcode::code39('text to encode', '100px', '30px');

Currently it will always send the "Content-type: image/png" header and output the code. Future revisions may support writing to file, etc.




----------------------------------------------------------------------------------

    header('Content-type: image/png');

    require_once ROOT_PATH.'extend/phpqrcode.php';
    $url = urldecode($url);
    //生成二维码
    die( \QRcode::png($url) );



	include 'phpqrcode.php'; 
	$value = 'http://www.learnphp.cn'; //二维码内容 
	$errorCorrectionLevel = 'L';//容错级别 
	$matrixPointSize = 6;//生成图片大小 

	/生成二维码图片 
	QRcode::png($value, 'qrcode.png', $errorCorrectionLevel, $matrixPointSize, 2); 
	QRcode::png('http://www.learnphp.cn', 'qrcode.png', 'L', 6, 2); 