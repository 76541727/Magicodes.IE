
## Ŀǰ�����Ŀ�������ڵ������ռ�����ʾ�׶Σ��������죬�������õ�����������������������

 `Magicodes.IE.Stash` ���������Դ�� `Logstash`�������¾���

��ģ������ΪIE�û��������ڹ������棨�ű������������ `ת��` ����


Ŀǰ��֧�ֶ�̬���ݵ��룬��ӭ�������µ�������뷨��

## ����ģ��˵��

Ŀǰ����ģ���֧��Excel�ļ�����Դ����������֧�ָ��������Դ���磺csv�����ݿ����http�ӿڵȡ�

### ��Excel�ļ�����:

 ����ʱ������Ҫ׼������������
 - ����Դ�ļ� ��Ҫ�����ԭʼ���ݣ���
 - Dtoӳ�����
 
 ӳ�����������������Դ�е�ÿһ��,���ӳ�䵽Dto�е����ԣ��ڹ��������ͨ�� `ת����` �ܵ������������ж��ת�����������Ϊ��Ҫ��ֵ��

 `ת����` ��һ�δ����ص�C#�ű������Ե���������Ŀ���Ѷ���Ŀ�ͷ�����Ϊ�����ṩ���������ԡ�

 #### �������̣�
  - ʵ�������棺 ``` var _excelImporter = new Magicodes.IE.Stash.Import.ExcelImporter(); ```
  - ��ȡӳ����� ``` var _mappingRules = _excelImporter.LoadDefinitionFromExcelFile("ӳ������ļ�·��"); ```
  - ����ӳ�����```  _excelImporter.Build(); ``` 
  // ����ʱ������������еĽű�������ִ�������ģ�ͬʱ�����ж���ı���Ҳ��������ֵ��
  - ��ȡ����Դ�� var _data = _excelImporter.Resolve("����Դ�ļ�·��");

  `_data` ��Ϊ��������ݣ�����Ϊ `List<object>`�� ���������ʵ������Ϊ������ָ����Dto���͡�

### ��дӳ�����
ӳ�������Էŵ������ļ���Ҳ���Էŵ�����Դһ�� ```_excelImporter.LoadDefinitionFromExcelFile()``` �����ṩ�������أ�������ȷָ���������Sheet���ƣ������ָ�������Դ�Ĭ�ϵ���Ϊ`$definition$`�Ĺ������л�ȡ����

ӳ�����������Щ������
- ����������ռ䣺��ָ���������ռ�����`using`���ű����������У��磺`Magicodes.IE.Stash.Import; Magicodes.IE.StashTests.Extensions`��
- Ŀ��Dto���ͣ�����Դ�е�ÿһ�н����Ϊ������͵�ʵ�������ʹ�ô������ռ��ȫ�����磺`MyProject.Dtos.StudentDto`��
- �������壺 ������ӳ������ж���ȫ�ֱ�����������ֵ�����ǳ�����Ҳ�����Ǵ����صĽű����������Ա������������ط��Ľű����á�

��������壬��ο���Ԫ�����ļ��� `Magicodes.IE.StashTests\_res\��ȷ�Ķ���.xlsx`��

## TODO:
- �ع���Ŀ���淶�ӿںͱ�������������ȡ����ӿڡ�
- ����Dto���룬ֱ�ӷ���ԭʼ���ݼ��ϡ�
- ֧�ִ�csv�ļ����롣
- ֧�ִ����ݿ�����롣
- ֧�ִ�http�ӿڵ��롣
- ֧������ע�룬�ű�����ֱ�Ӵ�DI��������Ҫ�ķ���
- ��ǿ��ȫ�ԡ�
- ��̬������
