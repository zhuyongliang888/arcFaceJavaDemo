1.
Windows:�뽫SDK��Ķ�̬��ŵ�readme.txtͬ��Ŀ¼��
Linux:�뽫SDK��Ķ�̬��ŵ� {readme.txtͬ��Ŀ¼}/bin/linux-x86-64/ Ŀ¼��
2.32λSDK����ʹ��32λ��jre,64λSDK����ʹ��64λ��jre,�����ʧ�ܡ�
3.����jna-4.4.0
4.�����ú�APPID FD_SDKKEY FR_SDKKEY
	public static final String    APPID  = "XXXXXXXXXX";
	public static final String FD_SDKKEY = "YYYYYYYYYY";
	public static final String FR_SDKKEY = "WWWWWWWWWW";
5.�����ú�ͼ���ļ�·����ͼ���С����ɫ��ʽ
    ����ͼ֧��YUV JPG PNG BMP
    if(bUseRAWFile){
        String filePathA = "640x480_I420.YUV";
        int yuv_widthA = 640;
        int yuv_heightA = 480;
        int yuv_formatA = ASVL_COLOR_FORMAT.ASVL_PAF_I420;
        
        String filePathB = "640x360_I420.YUV";
        int yuv_widthB = 640;
        int yuv_heightB = 360;
        int yuv_formatB = ASVL_COLOR_FORMAT.ASVL_PAF_I420;
        
        inputImgA = loadRAWImage(filePathA,yuv_widthA,yuv_heightA,yuv_formatA);
        inputImgB = loadRAWImage(filePathB,yuv_widthB,yuv_heightB,yuv_formatB);
    }else{
        String filePathA = "fgg_003.jpg";
        String filePathB = "003.jpg";
        
        inputImgA = loadImage(filePathA);
        inputImgB = loadImage(filePathB);
    }
6.AFR_FSDK_FACEMODEL���ݴ�ȡ����
    (1)������AFR_FSDK_FACEMODEL�л�ȡ����
       byte[] featureInByteArray = faceFeatureA.toByteArray();
    (2)��byte[]������AFR_FSDK_FACEMODEL
       AFR_FSDK_FACEMODEL faceFeatureX = AFR_FSDK_FACEMODEL.fromByteArray(featureInByteArray);

