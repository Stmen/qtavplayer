һ��ʹ��qt��ffmpeg��д�Ķ�ý�岥��������Ⱦ����opengl,Ŀǰֻ֧��qml�����Ŀǰ�������������ţ��϶����ţ����ſ��Ƶȹ��ܡ�
ʹ�÷���:
	1:�����pro��Ŀ���浼�����Ŀ:
		����
		include ($$PWD/qtavplayer/qtavplayer.pri)
	2.��main��������ע��qml���
		����
		qmlRegisterType<AVPlayer>("qtavplayer", 1, 0, "AVPlayer");
		qmlRegisterType<AVOutput>("qtavplayer", 1, 0, "AVOutput");
	3.��QML����ʹ�ô����
		��:
		import qtavplayer 1.0
		
		AVOutput{
			source: avplayer
		}
		
		AVOutput{ //����ͬʱ�ڶ�������ϲ���һ����Ƶ
			source: avplayer
		}
		AVPlayer{
			id : avplayer
			source : "url"
		}