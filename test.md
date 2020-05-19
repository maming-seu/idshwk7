

test：
    嵌入方法：
        直接利用16进制修改器对无用的空间进行编辑，直接写入16进制的base64编码后的隐藏信息
    提取方法：
        用16进制编辑器打开，在头文件之后发现很明显的字符串2!!NTcxMTcyMjTpqazpuKPlroc=22222222222222222222222222
        将  NTcxMTcyMjTpqazpuKPlroc=    base64解码得到  57117224马鸣宇
        或者使用strings但是还要再找


result2:
    嵌入方法：
        cmd —— LSBSteg.py encode -i origin.jpg -o result1.png -f info.txt（此处的origin.jpg并没有放到github上，不是这个库中的origin.jpg）
    提取方法：
        cmd —— LSBSteg.py decode -i result1.png -o 1.txt
        1.txt内容为：57117224mamingyu


result3：
    嵌入方法：
        cmd —— encode.py --image origin.jpg --watermark hide.png --result result3.png（
    提取方法：
        cmd —— decode.py --image result3.png --orig origin.jpg --result result.png
        result.png 内容为 57117224马鸣宇