# Calculadora
<?xml version="1.0"?>
<flowgorithm fileversion="4.2">
    <attributes>
        <attribute name="name" value="Calculadora"/>
        <attribute name="authors" value="op87"/>
        <attribute name="about" value=""/>
        <attribute name="saved" value="2026-08-27 04:46:53 "/>
        <attribute name="created" value="b3A4NztERVNLVE9QLU9QMDQ7MjAyNi0wOC0yNDsiMDE6NTI6MzUgIjsyMzcx"/>
        <attribute name="edited" value="b3A4NztERVNLVE9QLU9QMDQ7MjAyNi0wOC0yNzsiMDQ6NDY6NTMgIjs1OzI0OTI="/>
    </attributes>
    <function name="Main" type="None" variable="">
        <parameters/>
        <body>
            <while expression="true">
                <declare name="Opcao" type="Integer" array="False" size=""/>
                <output expression="&quot;Digite o n&#250;mero da opera&#231;&#227;o correspondente para acess&#225;-la: 1 para adi&#231;&#227;o, 2 para subtra&#231;&#227;o, 3 para multiplica&#231;&#227;o, 4 para divis&#227;o, 5 para potencia&#231;&#227;o, 6 para raiz quadrada, 7 para raiz c&#250;bica, 8 para porcentagem, 9 para calcular um aumento em percentual, 10 para calcular um desconto em percentual, 11 para fatorial, 12 para o valor de Pi, 13 para logaritmo, 14 para calcular o seno de um &#226;ngulo, 15 para calcular o cosseno de um &#226;ngulo, 16 para calcular a tangente de um &#226;ngulo, 17 para MMC, 18 para MDC, 19 para tranformar Celsius em Fahrenheit, 20 para transformar Fahrenheit em Celsius&quot;" newline="True"/>
                <input variable="opcao"/>
                <if expression="opcao==1">
                    <then>
                        <call expression="ExecutarAdicao"/>
                    </then>
                    <else>
                        <if expression="opcao==2">
                            <then>
                                <call expression="ExecutarSubtracao"/>
                            </then>
                            <else>
                                <if expression="opcao==3">
                                    <then>
                                        <call expression="ExecutarMultiplicacao"/>
                                    </then>
                                    <else>
                                        <if expression="opcao==4">
                                            <then>
                                                <call expression="ExecutarDivisao"/>
                                            </then>
                                            <else>
                                                <if expression="opcao==5">
                                                    <then>
                                                        <call expression="ExecutarPotenciacao"/>
                                                    </then>
                                                    <else>
                                                        <if expression="opcao==6">
                                                            <then>
                                                                <call expression="ExecutarRaizQuadrada"/>
                                                            </then>
                                                            <else>
                                                                <if expression="opcao==7">
                                                                    <then>
                                                                        <call expression="ExecutarRaizCubica"/>
                                                                    </then>
                                                                    <else>
                                                                        <if expression="opcao==8">
                                                                            <then>
                                                                                <call expression="ExecutarPercentual"/>
                                                                            </then>
                                                                            <else>
                                                                                <if expression="opcao==9">
                                                                                    <then>
                                                                                        <call expression="ExecutarAumentoPercentual"/>
                                                                                    </then>
                                                                                    <else>
                                                                                        <if expression="opcao==10">
                                                                                            <then>
                                                                                                <call expression="ExecutarDescontoPercentual"/>
                                                                                            </then>
                                                                                            <else>
                                                                                                <if expression="opcao==11">
                                                                                                    <then>
                                                                                                        <call expression="ExecutarFatorial"/>
                                                                                                    </then>
                                                                                                    <else>
                                                                                                        <if expression="opcao==12">
                                                                                                            <then>
                                                                                                                <call expression="ExecutarPi"/>
                                                                                                            </then>
                                                                                                            <else>
                                                                                                                <if expression="opcao==13">
                                                                                                                    <then>
                                                                                                                        <call expression="ExecutarLogaritmo"/>
                                                                                                                    </then>
                                                                                                                    <else>
                                                                                                                        <if expression="opcao==14">
                                                                                                                            <then>
                                                                                                                                <call expression="ExecutarSeno"/>
                                                                                                                            </then>
                                                                                                                            <else>
                                                                                                                                <if expression="opcao==15">
                                                                                                                                    <then>
                                                                                                                                        <call expression="ExecutarCosseno"/>
                                                                                                                                    </then>
                                                                                                                                    <else>
                                                                                                                                        <if expression="opcao==16">
                                                                                                                                            <then>
                                                                                                                                                <call expression="ExecutarTangente"/>
                                                                                                                                            </then>
                                                                                                                                            <else>
                                                                                                                                                <if expression="opcao==17">
                                                                                                                                                    <then>
                                                                                                                                                        <call expression="ExecutarMMC"/>
                                                                                                                                                    </then>
                                                                                                                                                    <else>
                                                                                                                                                        <if expression="opcao==18">
                                                                                                                                                            <then>
                                                                                                                                                                <call expression="ExecutarMDC"/>
                                                                                                                                                            </then>
                                                                                                                                                            <else>
                                                                                                                                                                <if expression="opcao==19">
                                                                                                                                                                    <then>
                                                                                                                                                                        <call expression="ExecutarCelsiusFahrenheit"/>
                                                                                                                                                                    </then>
                                                                                                                                                                    <else>
                                                                                                                                                                        <if expression="opcao==20">
                                                                                                                                                                            <then>
                                                                                                                                                                                <call expression="ExecutarFahreinheitCelsius"/>
                                                                                                                                                                            </then>
                                                                                                                                                                            <else>
                                                                                                                                                                                <output expression="&quot;Op&#231;&#227;o Inv&#225;lida!&quot;" newline="True"/>
                                                                                                                                                                            </else>
                                                                                                                                                                        </if>
                                                                                                                                                                    </else>
                                                                                                                                                                </if>
                                                                                                                                                            </else>
                                                                                                                                                        </if>
                                                                                                                                                    </else>
                                                                                                                                                </if>
                                                                                                                                            </else>
                                                                                                                                        </if>
                                                                                                                                    </else>
                                                                                                                                </if>
                                                                                                                            </else>
                                                                                                                        </if>
                                                                                                                    </else>
                                                                                                                </if>
                                                                                                            </else>
                                                                                                        </if>
                                                                                                    </else>
                                                                                                </if>
                                                                                            </else>
                                                                                        </if>
                                                                                    </else>
                                                                                </if>
                                                                            </else>
                                                                        </if>
                                                                    </else>
                                                                </if>
                                                            </else>
                                                        </if>
                                                    </else>
                                                </if>
                                            </else>
                                        </if>
                                    </else>
                                </if>
                            </else>
                        </if>
                    </else>
                </if>
            </while>
        </body>
    </function>
    <function name="ExecutarAdicao" type="None" variable="">
        <parameters/>
        <body>
            <declare name="a, b, c" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor do primeiro n&#250;mero: &quot;" newline="True"/>
            <input variable="a"/>
            <output expression="&quot;Digite o valor do segundo n&#250;mero: &quot;" newline="True"/>
            <input variable="b"/>
            <assign variable="c" expression="a+b"/>
            <output expression="c" newline="True"/>
        </body>
    </function>
    <function name="ExecutarAumentoPercentual" type="None" variable="">
        <parameters/>
        <body>
            <declare name="inicial, percentual, final" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor inicial: &quot;" newline="True"/>
            <input variable="inicial"/>
            <output expression="&quot;Digite o valor do aumento (%): &quot;" newline="True"/>
            <input variable="percentual"/>
            <if expression="percentual&lt;0">
                <then>
                    <output expression="&quot;O percentual n&#227;o pode ser negativo!&quot;" newline="True"/>
                </then>
                <else>
                    <assign variable="final" expression="inicial*(1+percentual/100)"/>
                    <output expression="final" newline="True"/>
                </else>
            </if>
        </body>
    </function>
    <function name="ExecutarCelsiusFahrenheit" type="None" variable="">
        <parameters/>
        <body>
            <declare name="celsius, fahrenheit" type="Real" array="False" size=""/>
            <output expression="&quot;Digite a temperatura em C&#176;: &quot;" newline="True"/>
            <input variable="celsius"/>
            <if expression="celsius&lt;-273.15">
                <then>
                    <output expression="&quot;O valor em &#176;C n&#227;o pode ser menor do que o zero absoluto (-273.15)&quot;" newline="True"/>
                </then>
                <else>
                    <assign variable="fahrenheit" expression="(celsius*9/5)+32"/>
                    <output expression="fahrenheit" newline="True"/>
                    <output expression="&quot;&#176;F&quot;" newline="True"/>
                </else>
            </if>
        </body>
    </function>
    <function name="ExecutarCosseno" type="None" variable="">
        <parameters/>
        <body>
            <declare name="angulo, cosseno, radiano" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor do &#226;ngulo em graus: &quot;" newline="True"/>
            <input variable="angulo"/>
            <assign variable="radiano" expression="angulo*Pi/180"/>
            <assign variable="cosseno" expression="Cos(radiano)"/>
            <output expression="cosseno" newline="True"/>
        </body>
    </function>
    <function name="ExecutarDescontoPercentual" type="None" variable="">
        <parameters/>
        <body>
            <declare name="inicial, percentual, final" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor inicial: &quot;" newline="True"/>
            <input variable="inicial"/>
            <output expression="&quot;Digite o valor do desconto (%): &quot;" newline="True"/>
            <input variable="percentual"/>
            <if expression="percentual&lt;0">
                <then>
                    <output expression="&quot;O percentual n&#227;o pode ser negativo!&quot;" newline="True"/>
                </then>
                <else>
                    <assign variable="final" expression="inicial*(1-percentual/100)"/>
                    <output expression="final" newline="True"/>
                </else>
            </if>
        </body>
    </function>
    <function name="ExecutarDivisao" type="None" variable="">
        <parameters/>
        <body>
            <declare name="numerador, denominador, quociente" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor do numerador: &quot;" newline="True"/>
            <input variable="numerador"/>
            <output expression="&quot;Digite o valor do denominador: &quot;" newline="True"/>
            <input variable="denominador"/>
            <if expression="denominador==0">
                <then>
                    <output expression="&quot;Erro! O denominador n&#227;o pode ser igual a zero (0)&quot;" newline="True"/>
                </then>
                <else>
                    <assign variable="quociente" expression="numerador/denominador"/>
                    <output expression="quociente" newline="True"/>
                </else>
            </if>
        </body>
    </function>
    <function name="ExecutarFahreinheitCelsius" type="None" variable="">
        <parameters/>
        <body>
            <declare name="fahrenheit, celsius" type="Real" array="False" size=""/>
            <output expression="&quot;Digite a temperatura em &#176;F: &quot;" newline="True"/>
            <input variable="fahrenheit"/>
            <if expression="fahrenheit&lt;-459.67">
                <then>
                    <output expression="&quot;O valor em &#176;F n&#227;o pode ser menor do que o zero absoluto (-459,67 &#176;F)&quot;" newline="True"/>
                </then>
                <else>
                    <assign variable="celsius" expression="(fahrenheit - 32)*5/9"/>
                    <output expression="celsius" newline="True"/>
                    <output expression="&quot;&#176;C&quot;" newline="True"/>
                </else>
            </if>
        </body>
    </function>
    <function name="ExecutarFatorial" type="None" variable="">
        <parameters/>
        <body>
            <declare name="numero, fatorial, contador" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor do n&#250;mero: &quot;" newline="True"/>
            <input variable="numero"/>
            <if expression="numero&lt;0">
                <then>
                    <output expression="&quot;Erro! N&#227;o existe fatorial de n&#250;mero negativo!&quot;" newline="True"/>
                </then>
                <else>
                    <assign variable="fatorial" expression="1"/>
                    <assign variable="contador" expression="1"/>
                    <while expression="contador&lt;=numero">
                        <assign variable="fatorial" expression="fatorial*contador"/>
                        <assign variable="contador" expression="contador+1"/>
                    </while>
                    <output expression="fatorial" newline="True"/>
                </else>
            </if>
        </body>
    </function>
    <function name="ExecutarLogaritmo" type="None" variable="">
        <parameters/>
        <body>
            <declare name="logaritmando, base, logaritmo" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor do logaritmando: &quot;" newline="True"/>
            <input variable="logaritmando"/>
            <if expression="logaritmando&lt;=0">
                <then>
                    <output expression="&quot;Erro! O logaritmando tem que ser maior do que zero(0)!&quot;" newline="True"/>
                </then>
                <else>
                    <output expression="&quot;Digite o valor da base: &quot;" newline="True"/>
                    <input variable="base"/>
                    <if expression="base&lt;=0">
                        <then>
                            <output expression="&quot;Erro! A base deve ser maior do que zero(0)!&quot;" newline="True"/>
                        </then>
                        <else>
                            <if expression="base==1">
                                <then>
                                    <output expression="&quot;Erro! A base n&#227;o pode ser igual a um(1)!&quot;" newline="True"/>
                                </then>
                                <else>
                                    <assign variable="logaritmo" expression="Log(logaritmando)/Log(base)"/>
                                    <output expression="logaritmo" newline="True"/>
                                </else>
                            </if>
                        </else>
                    </if>
                </else>
            </if>
        </body>
    </function>
    <function name="ExecutarMDC" type="None" variable="">
        <parameters/>
        <body>
            <declare name="a, b, c, mdc" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor do primeiro n&#250;mero: &quot;" newline="True"/>
            <input variable="a"/>
            <output expression="&quot;Digite o valor do segundo n&#250;mero: &quot;" newline="True"/>
            <input variable="b"/>
            <if expression="a&lt;=0 or b&lt;=0">
                <then>
                    <output expression="&quot;ATEN&#199;&#195;O! nenhum dos dois n&#250;meros pode ser menor ou igual a zero(0)&quot;" newline="True"/>
                </then>
                <else>
                    <while expression="b!=0">
                        <assign variable="c" expression="a%b"/>
                        <assign variable="a" expression="b"/>
                        <assign variable="b" expression="c"/>
                    </while>
                    <assign variable="mdc" expression="a"/>
                    <output expression="mdc" newline="True"/>
                </else>
            </if>
        </body>
    </function>
    <function name="ExecutarMMC" type="None" variable="">
        <parameters/>
        <body>
            <declare name="a, b, mmc" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor do primeiro n&#250;mero: &quot;" newline="True"/>
            <input variable="a"/>
            <output expression="&quot;Digite o valor do segundo n&#250;mero: &quot;" newline="True"/>
            <input variable="b"/>
            <if expression="a&lt;=0 or b&lt;=0">
                <then>
                    <output expression="&quot;ATEN&#199;&#195;O! nenhum dos dois n&#250;meros pode ser menor ou igual a zero(0)&quot;" newline="True"/>
                </then>
                <else>
                    <assign variable="mmc" expression="a"/>
                    <while expression="mmc%b!=0">
                        <assign variable="mmc" expression="mmc+a"/>
                    </while>
                    <output expression="mmc" newline="True"/>
                </else>
            </if>
        </body>
    </function>
    <function name="ExecutarMultiplicacao" type="None" variable="">
        <parameters/>
        <body>
            <declare name="a, b, produto" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor do primeiro n&#250;mero: &quot;" newline="True"/>
            <input variable="a"/>
            <output expression="&quot;Digite o valor do segundo n&#250;mero: &quot;" newline="True"/>
            <input variable="b"/>
            <assign variable="produto" expression="a*b"/>
            <output expression="produto" newline="True"/>
        </body>
    </function>
    <function name="ExecutarPercentual" type="None" variable="">
        <parameters/>
        <body>
            <declare name="a, b" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor do n&#250;mero: &quot;" newline="True"/>
            <input variable="a"/>
            <assign variable="b" expression="a/100"/>
            <output expression="b" newline="True"/>
        </body>
    </function>
    <function name="ExecutarPi" type="None" variable="">
        <parameters/>
        <body>
            <declare name="p" type="Real" array="False" size=""/>
            <assign variable="p" expression="Pi"/>
            <output expression="p" newline="True"/>
        </body>
    </function>
    <function name="ExecutarPotenciacao" type="None" variable="">
        <parameters/>
        <body>
            <declare name="base, expoente, resultado" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor da base: &quot;" newline="True"/>
            <input variable="base"/>
            <output expression="&quot;Digite o valor do expoente: &quot;" newline="True"/>
            <input variable="expoente"/>
            <assign variable="resultado" expression="base^expoente"/>
            <output expression="resultado" newline="True"/>
        </body>
    </function>
    <function name="ExecutarRaizCubica" type="None" variable="">
        <parameters/>
        <body>
            <declare name="base, resultado, sinal" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor da base: &quot;" newline="True"/>
            <input variable="base"/>
            <if expression="base&gt;=0">
                <then>
                    <assign variable="resultado" expression="base^(1/3)"/>
                </then>
                <else>
                    <assign variable="resultado" expression="(-base)^(1/3)"/>
                    <assign variable="resultado" expression="-resultado"/>
                </else>
            </if>
            <output expression="resultado" newline="True"/>
        </body>
    </function>
    <function name="ExecutarRaizQuadrada" type="None" variable="">
        <parameters/>
        <body>
            <declare name="base, resultado" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor da base: &quot;" newline="True"/>
            <input variable="base"/>
            <if expression="base&lt;0">
                <then>
                    <output expression="&quot;Erro! A base na raiz quadrada n&#227;o pode ser um n&#250;mero negativo!&quot;" newline="True"/>
                </then>
                <else>
                    <assign variable="resultado" expression="base^0.5"/>
                    <output expression="resultado" newline="True"/>
                </else>
            </if>
        </body>
    </function>
    <function name="ExecutarSeno" type="None" variable="">
        <parameters/>
        <body>
            <declare name="angulo, seno, radiano" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor do &#226;ngulo em graus: &quot;" newline="True"/>
            <input variable="angulo"/>
            <assign variable="radiano" expression="angulo*Pi/180"/>
            <assign variable="seno" expression="Sin(radiano)"/>
            <output expression="seno" newline="True"/>
        </body>
    </function>
    <function name="ExecutarSubtracao" type="None" variable="">
        <parameters/>
        <body>
            <declare name="a, b, c" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor do primeiro n&#250;mero: &quot;" newline="True"/>
            <input variable="a"/>
            <output expression="&quot;Digite o valor do segundo n&#250;mero: &quot;" newline="True"/>
            <input variable="b"/>
            <assign variable="c" expression="a-b"/>
            <output expression="c" newline="True"/>
        </body>
    </function>
    <function name="ExecutarTangente" type="None" variable="">
        <parameters/>
        <body>
            <declare name="angulo, tangente, cosseno, radiano" type="Real" array="False" size=""/>
            <output expression="&quot;Digite o valor do &#226;ngulo em graus: &quot;" newline="True"/>
            <input variable="angulo"/>
            <assign variable="radiano" expression="angulo*Pi/180"/>
            <assign variable="cosseno" expression="Cos(radiano)"/>
            <if expression="Abs(cosseno)&gt;0.000001">
                <then>
                    <output expression="&quot;A tangente n&#227;o pode ser definida por esse &#226;ngulo&quot;" newline="True"/>
                </then>
                <else>
                    <assign variable="tangente" expression="Tan(radiano)"/>
                    <output expression="tangente" newline="True"/>
                </else>
            </if>
        </body>
    </function>
</flowgorithm>
