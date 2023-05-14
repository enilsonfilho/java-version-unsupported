# Java - Unsupported Class File Version

## Problema

Ao compilar ou executar um código Java, você pode encontrar o erro "Unsupported class file major version". Isso ocorre quando o arquivo de classe (*.class) foi compilado com uma versão do Java que é superior à versão do Java em que você está tentando executá-lo.

## Solução

A tabela a seguir mostra as versões do Java e suas respectivas versões de arquivo de classe:

| Versão do Java	| Versão do Arquivo de Classe 
| --------------  | --------------------------- 
| Java SE 19	    | 63                          
| Java SE 18	    | 62
| Java SE 17	    | 61
| Java SE 16	    | 60
| Java SE 15	    | 59
| Java SE 14	    | 58
| Java SE 13	    | 57
| Java SE 12	    | 56
| Java SE 11	    | 55
| Java SE 10	    | 54
| Java SE 9	      | 53
| Java SE 8	      | 52
| Java SE 7	      | 51
| Java SE 6.0	    | 50
| Java SE 5.0	    | 49
| JDK 1.4	        | 48
| JDK 1.3	        | 47
| JDK 1.2	        | 46
| JDK 1.1	        | 45

Para resolver o erro "Unsupported class file major version", siga uma das opções abaixo:

1. Atualize sua versão do Java para uma versão compatível com a versão do arquivo de classe. Por exemplo, se você estiver tentando executar um arquivo de classe compilado com a versão 59, certifique-se de ter o Java SE 15 ou superior instalado.

2. Verifique a versão do Java em que você está tentando compilar ou executar o código e ajuste a configuração de compilação para a versão correta. Por exemplo, se você estiver usando o Maven, verifique a configuração do compilador no arquivo pom.xml. Se estiver usando o Gradle, verifique a configuração no arquivo build.gradle.

```
<!-- Exemplo de configuração do compilador no Maven -->
<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-compiler-plugin</artifactId>
            <version>3.8.1</version>
            <configuration>
                <source>15</source>
                <target>15</target>
            </configuration>
        </plugin>
    </plugins>
</build>
```
```
// Exemplo de configuração do compilador no Gradle
plugins {
    id 'java'
}

java {
    sourceCompatibility = JavaVersion.VERSION_15
    targetCompatibility = JavaVersion.VERSION_15
}
```

Certifique-se de ajustar as configurações de compilação de acordo com a versão do Java que você deseja utilizar.

## Observações

- É importante manter seu ambiente de desenvolvimento atualizado com as versões mais recentes do Java para aproveitar os recursos e correções de bugs mais recentes.
- Certifique-se de compilar e executar seu código com uma versão compatível do Java para evitar o erro "Unsupported class file major version".
