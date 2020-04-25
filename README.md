# freerubles
$option = array( 
    //First row
array(
$telegram->buildInlineKeyBoardButton("دکمه 1", $url="http://link1.com"), $telegram->buildInlineKeyBoardButton("دکمه 2", $url="http://link2.com")
), 
    //Second row 
 array(
 $telegram->buildInlineKeyBoardButton("Button 3", $url="http://link3.com"), $telegram->buildInlineKeyBoardButton("Button 4", $url="http://link4.com"), $telegram->buildInlineKeyBoardButton("@Mohsen322", $url="http://link5.com")
 ), 

    //Third row
   array(
           $telegram->buildInlineKeyBoardButton("www.Virgool.io", $url="http://link6.com")
   ) 
    );
$keyb = $telegram->buildInlineKeyBoard($option);
$content = array('chat_id' => $chat_id, 'reply_markup' => $keyb, 'text' => "آموزش ساخت دکمه شیشه ای");
$telegram->sendMessage($content);
