## һ.jQuery�Ļ���ʹ��

  ->1.0  2.0  3.0   �ֱ�֧��ie8  ����֧��ie8  ȫ����֧��ie8  ������ʱ����õ���1.���汾
  ->��Ϊ�����汾��ѹ���汾  ����min����ѹ���汾��һ�������ʹ�õ��ǿ����汾
  ->window.onload=function(){}    <=>    $(function(){})   ���ĵ�������ɵļ���
  ->��Ϊ����ʹ��     ʹ��jQuery���ĺ�������jQuery���Ķ���    ���ĺ���$/jQuery   ���Ķ��� ִ��$()���صĶ���

## ��.jQuert����������

  ->jQuery�ĺ��ĺ���,ֱ�ӿ���
  ->jQuery�ĺ��Ķ���,ִ��jQuery����������

## ��.jQuery������ʹ��

  I.��Ϊһ�㺯��ʹ��:$(param)
	1).  ����Ϊ����  :  ��DOM������ɺ�ִ�д˻ص�����
	2).  ����ΪDOM����  : ��DOM�����װ��jQuery����
	3).  ����Ϊѡ�����ַ��� : ��������ƥ��ı�ǩ���������Ƿ�װ��jQuery����
	4).  ����Ϊhtml��ǩ�ַ���  : (�õ���)������ǩ���󲢷�װ��jQuery����

  II.��Ϊ����ʹ��:$.xxx()
	1).  $.each() :  ��ʹ��������     �ص������е�һ��Ϊkey���ڶ���Ϊvalue
    2).  $.trim() :  ȥ�����˿ո�     
	
  III. �¼��ص�������   thisָ����� #btn  DOM����Ԫ��

## ��.jQuery�����ʹ��

	I. ���
	
	1).��ִ��jQuery���ĺ������صĶ���
	2).jQuery�����ڲ���������domԪ�ض����α����
	3).jQuery����ӵ�кܶ����õķ���������
	
	II. ������Ϊ
	
	1).size()/length : ������DOMԪ��
	2).[index]/get(index)  :  �õ�DOMԪ�ض�Ӧ���±�
	3).each()  :  ����DOMԪ��
	4).index()  :  �õ�DOMԪ�ص��±�
	
	III. α����
	
	1).α������һ������
	2).α���������length����
	3).�����������length��Ϊ0����ô����Ҫ�а����±�洢������
	4).û�������ر�ķ��� forEach() push() pop() splice()

## ��.jQuery����ѡ����

	1).class   ".b"�������е�class����Ϊb��Ԫ��
	2).id      "#div"  ����idԪ��
	3).��ǩ               "div"   �����ǩԪ��
	4).�Ӽ�               "div.box" ����class����Ϊbtn�е�divԪ��
	5).����               "#b,#c"  ����idΪc��idΪb��Ԫ��

## ��.jQuery���ѡ����

	I.������Ԫ�أ����Ԫ�أ��ֵ�Ԫ�ص�ѡ����
	
	1).  >   ��ָ��ǰ��һ������һ�������������´�
	2).  +   ��ָ��ǰԪ�ص���һ��Ԫ�أ�ֻ����һ��
	3).  ~   ��ָ��ǰԪ�صĺ��������ֵܽ���Ԫ��(���ǲ��ܰ�����һ����Ԫ��)

## ��.jQuery����ѡ����

	I. ѡ����
	
	1).  :first  ����
	2).  :last   ����
	3).  :not(.box)   ѡ�񲻰���clssΪbox��Ԫ��
	4).  :lt(3):gt(0)  С�ڵ��������ڵ����
	5).  :contains("name")  ѡ�����б�ǩ��innerHTML������name�ı�ǩ
	6).  :hidden()  ѡ�����صı�ǩ
	7).  [title]  ѡ�����д���title���Եı�ǩ��
	8).  [title=hello]  ѡ��title����Ϊhello�ı�ǩ
	
	II.  ���ѡ��������ͬʱִ�У������Դ�ִ��

## ��.jQuery���л�ɫ

	1).   odd:ż��       even:����    nth-child(2n)ż��

## ��.jQuery��ѡ����

	I.���ĳ���ѡ����
		
	1).  text[disabled]  :ѡ��text�ı��Ĳ����������
	2).  checkbox:checked  :ѡ��ѡ�еĸ�ѡ��ť  
	
	II. :�ȼ���[]   ��ѡ�����еȼ۴���

## ʮ.jQuery_$���߷���

	I.���߷���
	
	1).  $.each()  :  ������������е�����
	2).  $.trim()  :  ȥ���ַ�������Ŀո�
	3).  $.type(obj) : �õ���������
	4).  $.isArray(obj) : �ж��Ƿ�������
	5).  $.isFunction(obj) : �ж��Ƿ��Ǻ���
	6).  $.parseJSON(json) : ����json�ַ���ת��Ϊjs����
	
	II. JSON
	
	1).  '{"name":"Tom" , "Age":12 }'  ����һ��json 
	2).  '[{"name":"Tom","Age":12},{"name":"Allen","Age":24}]'   ����һ��json����
	3).   JSON.parse(jsonString)  json�ַ���---->js����/����
	4).   JSON.stringify(jsObj/jsArr)  js����/����---->json�ַ���

## ʮһ.jQuery��tab����л�

	I.  ���˼·    ��ȡȫ����DOMԪ�أ�Ȼ��ͨ��this��ȡ�����index()�����ͨ������jQuery������±�ķ�ʽ����
	
	II.  �Ȼ�ȡȫ����DOMԪ�أ�Ȼ����һ����ǰ��ʾ��Ԫ�ص��±꣬�������Ԫ�����أ�����ʾ��ǰ�����Ԫ�أ��������±꣨Ч���ϸ��ߣ�

## ʮ��.jQuery����

	I.����
	
	1).attr()  һ����������鿴��������������ڶ�����������    ���ǲ��ܲ�������ֵ
	2).removeAttr()  �Ƴ�
	3).addClass()  ���class 
	4).html()   ��ǩ   ���ַ�������->���Ǳ�ǩ��
	5).prop()   ר�Ų�������ֵΪboolean������ֵ

## ʮ��.jQuery��CSS����

	I.CSS����
	
	1).css()   һ����������鿴��������������ڶ�����������  
	2).css({'color':'#ff0011'})�������Ƕ��ֵ

## ʮ��.jQueryλ�ò���

	I.offset ��   position
	
	1).offset().left ��  offset().top  �������Ի�ȡ�����ҳ���λ��
	2).position()  ��������һ���������ȡ���Ǹ�Ԫ�ص�λ��

## ʮ��.jQuery�е�λ�ù���

	I.���÷���
	
	1).scrollTop()  ���Եõ�Ԫ�صĹ����߶�
	2).scrollLeft()   ���Եõ�x���������
	3).�������������(number)  �ȿ����ù����ľ���
	
	II.��λ�ȡ�������       ��ȡҳ���html+body�����������Ĺ�������

## ʮ��.��ϰ jQuery�ع�������

	I.˲��ص�����   $('html,body').scrollTop(0)
	II.ƽ������    ������ʱ�䣬ʱ��������ʱ����ʱ�䣩�ܾ��� ÿ���ƶ��ľ��루�ܾ��������Ҫ��ʱ�䣩  Ȼ���ö�ʱ��ִ��

## ʮ��.jQueryԪ�صĳߴ�

	I.���ݳߴ�
	
	1).height() :height
	2).width()  :width
	
	II.�ڲ��ߴ�
	
	1).innerHeight() :height+padding
	2).innerWidth()  :width+padding
	
	III.�ⲿ�ߴ�
	
	1).outerHeight(false/true)  :height+padding+border  �����true������margin
	1).outerWidth(false/true)  :width+padding+border  �����true������margin

## ʮ��.jQuery��ɸѡ

	I.����
	
	1).first()  ��һ��
	2).last()  ���һ��
	3).eq()*  ָ��ĳһ��  ����Ϊnumber  
	4).filter('[title=hello]')  ָ��title����Ϊhello��
	5).not('[title=hello]')   ָ������hello��(������û��title����)
	6).filter('[title][title!=hello]')   ����ѡ����������������
	7).has('span')   ָ���ڲ���ǩ
	
	II.����
	
	1).children()  �ӱ�ǩ  
	2).find()      �����ǩ
	3).parent()    ����ǩ
	4).prevAll()   ǰ��ı�ǩ
	5).siblings()  �ֵܱ�ǩ

## ʮ��.jQuery�ĵ����� *

	I.��ɾ��
	
	1).append(ELement)   ���ڲ�������Ԫ��
	2).prepend(Element)  ���ڲ���ǰ���Ԫ��
	3).before(Element)   ���ֵ�ǰ�����Ԫ��
	4).after(ELement)    ���ֵܺ������Ԫ��
	5).replaceWith(Element)   �滻ָ�����ڲ�Ԫ��
	6).remove(DOM_Element)    �Ƴ�ָ�����ڲ�Ԫ��

## ��ʮ.jQuery�¼�����

```js
I.�����¼�

1).mouseenter()    �������
2).mouseleave()    ����Ƴ�

II.�¼�����

1).on(eve,fn)      ��һ�����������¼��Ĵ���ʽ
2).off()           �͵�һ�����Ӧ��ȡ��ʱ���
3).���ʱ����ev 
	->ev.clientX     ���ͻ������Ͻǵľ���
	->ev.pageX       ��ҳ�涥�����Ͻǵľ���
	->ev.offsetX     ��������¼����Ͻǵľ���
	->ev.stopPropagation()    ��ֹ�¼���ð��
	->ev.preventDefault()     ��ֹ�¼���Ĭ����Ϊ

III.�¼��л�

1).hover(fn,fn)     ��mouseenter,mouseleave���������Ļص�����

IV.����mouseover��mouseenter

*mouseover:��������Ԫ��ʱҲ�ᴥ��,��Ӧmouseout
*mouseenter:ֻ�����뵱ǰԪ��ʱ����,��Ӧmouseleave

V.�¼�ί��

1).�������Ԫ��(li)���¼�����ί�и���Ԫ��(ul)����
2).�����ص��Ǽ����˸�Ԫ����
3).�������κ�һ����Ԫ��(li)ʱ���¼���ð�ݵ���Ԫ��(ul)��
4).����Ԫ�ز���ֱ�Ӵ������Ǹ���event.target�õ������¼�����Ԫ��(li)��ͨ�������Ԫ�ص����¼��ص�����
5).ί�з� ��  ҵ��     li
6).��ί�з�  :   �н�    ul
7).����µ���Ԫ�أ��Զ����¼���Ӧ����
8).�����¼�����������:    n==>1
9).�����¼�ί��API: $(parentSelector).delegate(childrenSelector,eventName,callback)
10).ȡ���¼���ί��API:$(parentSelector).undelegate(eventName)

VI. �¼�����
1).$('div').triggler('click',['data',[data]])
2).$('div').bind('click',function(e,param1,parma2))

```

## ��ʮһ.jQuery����

	I.���ö���
	
	1).fadeOut()   ����   param--->number  �����������    
	2).fadeIn()    ����   ����������һ��
	3).fadeToggle()  ���뵭���л�   ���Դ�һ���ص����������л�������ʱ�򴥷�
	4).���ϸı�Ԫ��opacity��ʵ��
	5).slideDown()   ��������չ��
	6).sildeUp()     ������������
	7).sildeToggle()   ���������л�չ��/����
	8).���ϸı�Ԫ��heightʵ��
	9).show()     ��ʾ
	10).hide()    ����
	11).toggle()  �л�
	12).���ϸı�opacity��height��widthʵ��
	
	II.�Զ��嶯��
	
	1).animate()    ָ���Զ��嶯��  �������Դ�һ��json �ֱ�ָ��ֵ
	2).animate()    ����Ҫ���е�λ�������Խ����ַ����ļӼ�
	3).stop()       ������ֹ�����ļ�������

## ��ʮ��.jQuery��⹲��

	I.�����$��ͬʱ����ʱ,��Ҫʹ��
	II.����jQuery.noConflict()�ͷ�$ʹ��Ȩ
	III.������Ҫ���õ�$ʱ��ֻ��ʹ��jQuery

## ��ʮ��.����onload��ready

	I.window.onload
	
	1).����ҳ���ͼƬ�������Ż����(��)
	2).ֻ����һ�������ص�
	
	II.$(document).ready()
	
	1).��ͬ��$(function(){})
	2).ҳ�������ͻص�(��)
	3).�����ж�������ص�

## ��ʮ��.jQuery��չ����

	I.$��չ����, ʹ�÷�ʽ---->$.min()  
	
	1).����
	$.extend({
		xx:function(){
			...
		},
		yy:function(){
			...
		}
	})
	
	II.$����µķ���,ʹ�÷�ʽ----->$.checkAll()
	
	1).���� 
	$.fn.extend({
		xx:function(){
			...
		},
		yy:function(){
			...
		}
	})
