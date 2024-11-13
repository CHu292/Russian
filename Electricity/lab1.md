
# 2. Когда переходной процесс считается завершенным (теоретически и практически)?


### Теоретическое завершение переходного процесса
 Kết thúc lý thuyết của quá trình quá độ
 
В **теоретическом** плане, переходной процесс считается завершённым, когда все временные составляющие отклика цепи полностью затухают, и система достигает нового **установившегося состояния**. Это состояние определяется, когда мгновенные значения тока и напряжения приближаются к новым стационарным значениям, соответствующим новым входным условиям или после внешнего воздействия. 

_Về mặt **lý thuyết**, quá trình quá độ được coi là kết thúc khi tất cả các thành phần thời gian của phản ứng mạch tắt hoàn toàn và hệ thống đạt đến trạng thái **ổn định mới**. Trạng thái này được xác định khi giá trị tức thời của dòng điện và điện áp tiến đến các giá trị ổn định mới, tương ứng với các điều kiện đầu vào mới hoặc sau tác động từ bên ngoài._

В линейных цепях с элементами **R, L и C** переходной процесс часто описывается экспоненциальной функцией вида $$e^{-\alpha t}$$, где $$\alpha$$ — коэффициент затухания. В этом случае отклик асимптотически стремится к нулю по мере удаления во времени, но математически не достигает его полностью, что позволяет считать процесс завершённым лишь приближённо.

_Trong các mạch tuyến tính với các phần tử **R, L và C**, quá trình quá độ thường được mô tả bằng hàm mũ dạng $$e^{-\alpha t}$$, trong đó \$$alpha$$ là hệ số suy giảm. Trong trường hợp này, đáp ứng tiến dần về 0 theo thời gian, nhưng về mặt toán học sẽ không bao giờ đạt đến hoàn toàn, do đó quá trình chỉ có thể được coi là kết thúc một cách xấp xỉ._

### Практическое завершение переходного процесса
Kết thúc thực tế của quá trình quá độ

**Практически** переходной процесс считается завершённым, когда изменения параметров системы становятся настолько малы, что их можно пренебречь в пределах допустимой погрешности измерений или расчётов. 

_Về mặt **thực tế**, quá trình quá độ được coi là kết thúc khi các thay đổi về thông số của hệ thống trở nên nhỏ đến mức có thể bỏ qua trong giới hạn sai số cho phép của phép đo hoặc tính toán._

В большинстве случаев, для **цепей первого порядка** (например, RC и RL-цепей) используется правило $$5\tau$$ (пять постоянных времени):
- $$\tau = RC$$ для RC-цепей,
- $$\tau = \frac{L}{R}$$ для RL-цепей.

_Trong hầu hết các trường hợp, đối với **mạch bậc nhất** (chẳng hạn như mạch RC và RL), người ta thường sử dụng quy tắc $$5\tau$$ (năm hằng số thời gian):_
- $$\tau = RC$$ cho mạch RC,
- $$\tau = \frac{L}{R}$$ cho mạch RL.


Через время, равное пяти постоянным времени ($$t = 5\tau$$), переходной процесс достигает более 99% от своего окончательного значения, что обычно считается достаточным приближением к установившемуся состоянию.

_Sau thời gian bằng năm lần hằng số thời gian ( $$t = 5\tau$$)), quá trình quá độ đạt đến hơn 99% giá trị cuối cùng, thường được coi là đủ để tiến gần đến trạng thái ổn định._

### Обоснования и примеры из документов
Документы по схемотехнике, например, учебник Милениной и практикумы по лабораторным работам, содержат методики для анализа завершения переходного процесса в различных цепях. На практических занятиях, где используются осциллографы для анализа переходных процессов, обычно считается, что переходный процесс завершён, когда осциллограмма сигнала стабилизируется на уровне установившегося значения с небольшими отклонениями в пределах 1–2% от этого значения. 

При моделировании и расчетах переходных процессов в лабораторных работах на практике также применяется метод $$5\tau$$, так как этот подход обеспечивает достижение стабильного уровня, приемлемого для инженерных расчётов и анализа.

 Giải thích và ví dụ từ các tài liệu
 
Các tài liệu về kỹ thuật mạch điện, chẳng hạn như giáo trình của Milenina và các hướng dẫn thực hành thí nghiệm, chứa các phương pháp phân tích để xác định quá trình quá độ kết thúc trong các mạch khác nhau. Trong các bài thực hành, khi sử dụng dao động ký để phân tích quá trình quá độ, người ta thường cho rằng quá trình quá độ đã kết thúc khi đồ thị dao động của tín hiệu ổn định ở mức giá trị ổn định với sai lệch nhỏ trong khoảng 1–2% so với giá trị đó.

Khi mô phỏng và tính toán quá trình quá độ trong các thí nghiệm, quy tắc $$5\tau$$ cũng thường được áp dụng vì cách tiếp cận này đảm bảo đạt mức ổn định phù hợp cho các phép tính kỹ thuật và phân tích.

--- 

# Явление сверхтоков и перенапряжений в переходных процессах: объяснение, формулы и графики
Hiện tượng dòng điện quá mức và quá điện áp trong các quá trình quá độ: giải thích, công thức và đồ thị


#### 1. Суть явления сверхтоков
 Bản chất của hiện tượng dòng điện quá mức


**Сверхтоки** возникают в цепях, содержащих индуктивные или ёмкостные элементы, при резком изменении входного сигнала (например, включении или выключении напряжения). Индуктивные элементы, такие как катушки, противодействуют изменению тока и могут приводить к резким всплескам тока при коммутации. Для индуктивного элемента с сопротивлением $$R$$ и индуктивностью $$L$$ это можно описать следующим дифференциальным уравнением:

_**Dòng điện quá mức** xuất hiện trong các mạch chứa các phần tử cảm kháng hoặc điện dung khi có sự thay đổi đột ngột của tín hiệu đầu vào (chẳng hạn, khi bật hoặc tắt điện áp). Các phần tử cảm kháng, chẳng hạn như cuộn cảm, chống lại sự thay đổi dòng điện và có thể dẫn đến sự tăng vọt của dòng điện khi đóng ngắt. Đối với phần tử cảm kháng có điện trở $$R$$ và độ tự cảm $$L$$, hiện tượng này có thể được mô tả bằng phương trình vi phân:_

$$
\frac{dI}{dt} + \frac{R}{L} I = \frac{V}{L}
$$

где $$V$$ — напряжение источника. В цепи RL ток $$I(t)$$ растет экспоненциально с постоянной времени $$\tau = \frac{L}{R}$$, и максимальное значение сверхтока может быть достигнуто на этапе заряда или разряда индуктивного элемента.

_trong đó $$V$$ là điện áp của nguồn. Trong mạch RL, dòng điện $$I(t)$$ tăng theo hàm mũ với hằng số thời gian $$\tau = \frac{L}{R}$$, và giá trị cực đại của dòng điện quá mức có thể đạt được ở giai đoạn nạp hoặc xả của phần tử cảm kháng._

#### 2. Суть явления перенапряжений
Bản chất của hiện tượng quá điện áp


**Перенапряжения** возникают чаще всего в цепях с ёмкостями (конденсаторами) и индуктивностями (катушками) в момент коммутации. В этих случаях реактивные элементы не позволяют мгновенно изменять ток или напряжение, что вызывает кратковременные всплески. В цепях RLC перенапряжения могут быть особенно значительными, если процесс приобретает колебательный характер, где напряжение на конденсаторе $$u_C(t)$$ определяется решением колебательного уравнения:

_**Quá điện áp** xuất hiện chủ yếu trong các mạch có điện dung (tụ điện) và cảm kháng (cuộn cảm) tại thời điểm đóng ngắt. Trong các trường hợp này, các phần tử phản kháng không cho phép thay đổi tức thì dòng điện hoặc điện áp, dẫn đến các xung tăng vọt trong thời gian ngắn. Trong các mạch RLC, hiện tượng quá điện áp có thể đặc biệt lớn nếu quá trình này trở thành dao động, với điện áp trên tụ $$u_C(t)$$ được xác định bằng nghiệm của phương trình dao động_ 

$$
u_C(t) = U_{\text{уст}} \left(1 - e^{-\alpha t} \cos(\omega_d t + \phi)\right)
$$

где $$\alpha = \frac{R}{2L}$$ — коэффициент затухания, а $$\omega_d = \sqrt{\frac{1}{LC} - \left(\frac{R}{2L}\right)^2}$$ — частота колебаний.

_trong đó $$\alpha = \frac{R}{2L}$$ là hệ số suy giảm và $$\omega_d = \sqrt{\frac{1}{LC} - \left(\frac{R}{2L}\right)^2}$$ là tần số dao động._

#### 3. Графики и схемы
 Đồ thị và sơ đồ



