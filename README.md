https://www.polarxiong.com/archives/Hadoop-Intellij%E7%BB%93%E5%90%88Maven%E6%9C%AC%E5%9C%B0%E8%BF%90%E8%A1%8C%E5%92%8C%E8%B0%83%E8%AF%95MapReduce%E7%A8%8B%E5%BA%8F-%E6%97%A0%E9%9C%80%E6%90%AD%E8%BD%BDHadoop%E5%92%8CHDFS%E7%8E%AF%E5%A2%83.html

ǰ��
Hadoop��������������ģʽ�£�

����ģʽ
α�ֲ�ģʽ
��ȫ�ֲ�ʽģʽ
���ų�ѧ������Hadoop�ĵ�һ�ÿξ���α�ֲ�ģʽHadoopϵͳ�İ�װ������һ����Ѫ��ʷ���ַ��̸̳�����װ����ʵ���ϣ�����Hadoop��MapReduce�����ڵ��������У�����һ����Ҫ��װα�ֲ�ģʽHadoopϵͳ������������һ����Ҫ��װHadoop��

���к͵���MapReduce����ֻ��Ҫ����Ӧ��Hadoop���������У�������ȫ����һ����ͨ��JAVA���򡣱��ľͽ��������ּ򵥷���ķ�����

���
����������˵���ڵ���ģʽ�£����Խ�MapReduce���򵱳�һ����ͨ��JAVA���򣻶Ա�α�ֲ�ģʽ������Ҫ���������û��Hadoop�������������ϵͳ����JobTracker��壬��ֻ���������к͵��Գ��򣻶����ŵ�����ڿ������Է��㣬��д�ĳ���ͨ������Ҫ�޸ļ�������ʵ�ķֲ�ʽHadoop��Ⱥ�����С�

Maven
Maven��һ����Ŀ�����ߣ�����������Ҫ�õ�����������������ϵͳ��ͨ�������ڿ���Hadoop MapReduce����ʱ������Ҫ���ض�Ӧ�汾�ľ���Ȼ����ؾ����е�JAR����������ʼ��д���롣�������˵�������׵��������������۸��ӵ�������ϵ��������Maven�������ɽ��������⡣ֻ��Ҫ��Maven�����ļ���ָ��Hadoop���������ֺͰ汾�ţ�Maven�����Զ��㶨��Щ��������ֻ��Ҫר��д����ͺ��ˡ�

Intellij IDEA
Ϊʲô����Eclipse�أ�����û�б��Eclipse����˼��ֻ������ΪEclipse�û�����̫����Ҹ��ֲ������ڷ�����Intellij��������˳�֣�������Maven��֧�֣����ҿ������ƺ�����ǰ������ʹ��Intellij�ˡ�

����Ҫ��
JDK 1.7��1.8�ƺ�Ҳ���ԣ���Hadoop�ٷ��Ƽ�1.7��
Intellij
����Ҫ��װ�κ�ģʽ��Hadoop��

WordCount
������Hadoop�Ĺٷ�ʾ������WordCountΪ������ʾ���һ������д����ֱ�����С�

�½���Ŀ
��Intellij�е��File->New->Project���ڵ����ĶԻ�����ѡ��Maven��JDKѡ��1.7�����Next��

Screenshot New Maven Project

��������дMaven��GroupId��ArtifactId���������Next��

Screenshot Project Info

Ȼ����Project name��������дWordCount�����Finish��

Screenshot New Maven Project

�������½�����һ���յ���Ŀ�����ż�������һ���ط�������Ҫ�޸ġ���Intellij��Preferenceƫ�����ã���λ��Build, Execution, Deployment->Compiler->Java Compiler����WordCount��Target bytecode version�޸�Ϊ1.7��

Screenshot Target Bytecode Version

��������
�½���Ŀ����Intellij���Ϸ�������Ŀ�ļ��ṹ��˫���Ա༭pom.xml�������Maven�������ˡ�

���Դ
pom.xml��ʼ��������

XML
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.polarxiong</groupId>
    <artifactId>hadoop</artifactId>
    <version>1.0-SNAPSHOT</version>

</project>
��project��β�����

XML
<repositories>
    <repository>
        <id>apache</id>
        <url>http://maven.apache.org</url>
    </repository>
</repositories>
���apacheԴ��

�������
����ֻ��Ҫ�õ���������hadoop-core��hadoop-common�������Ҫ��дHDFS������Ҫ����hadoop-hdfs��hadoop-client�������Ҫ��дHBase������Ҫ����hbase-client��

��project��β�����

XML
<dependencies>
    <dependency>
        <groupId>org.apache.hadoop</groupId>
        <artifactId>hadoop-core</artifactId>
        <version>1.2.1</version>
    </dependency>
    <dependency>
        <groupId>org.apache.hadoop</groupId>
        <artifactId>hadoop-common</artifactId>
        <version>2.7.2</version>
    </dependency>
</dependencies>
����hadoop-core��versionһ��Ϊ1.2.1��hadoop-common��version�����������ʵ����Ҫ����

�޸�pom.xml��ɺ�Intellij���Ͻǻ���ʾMaven projects need to be Imported�����Import Changes�Ը�������

����������pom.xml

XML
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.polarxiong</groupId>
    <artifactId>hadoop</artifactId>
    <version>1.0-SNAPSHOT</version>

    <repositories>
        <repository>
            <id>apache</id>
            <url>http://maven.apache.org</url>
        </repository>
    </repositories>

    <dependencies>
        <dependency>
            <groupId>org.apache.hadoop</groupId>
            <artifactId>hadoop-core</artifactId>
            <version>1.2.1</version>
        </dependency>
        <dependency>
            <groupId>org.apache.hadoop</groupId>
            <artifactId>hadoop-common</artifactId>
            <version>2.7.2</version>
        </dependency>
    </dependencies>
</project>
WordCount
��src->main->java���½�һ��WordCount�࣬�������

Java
import java.io.IOException;
import java.util.StringTokenizer;

import org.apache.hadoop.conf.Configuration;
import org.apache.hadoop.fs.Path;
import org.apache.hadoop.io.IntWritable;
import org.apache.hadoop.io.Text;
import org.apache.hadoop.mapreduce.Job;
import org.apache.hadoop.mapreduce.Mapper;
import org.apache.hadoop.mapreduce.Reducer;
import org.apache.hadoop.mapreduce.lib.input.FileInputFormat;
import org.apache.hadoop.mapreduce.lib.output.FileOutputFormat;

public class WordCount {

    public static class TokenizerMapper
            extends Mapper<Object, Text, Text, IntWritable> {

        private final static IntWritable one = new IntWritable(1);
        private Text word = new Text();

        public void map(Object key, Text value, Context context
        ) throws IOException, InterruptedException {
            StringTokenizer itr = new StringTokenizer(value.toString());
            while (itr.hasMoreTokens()) {
                word.set(itr.nextToken());
                context.write(word, one);
            }
        }
    }

    public static class IntSumReducer
            extends Reducer<Text, IntWritable, Text, IntWritable> {
        private IntWritable result = new IntWritable();

        public void reduce(Text key, Iterable<IntWritable> values,
                           Context context
        ) throws IOException, InterruptedException {
            int sum = 0;
            for (IntWritable val : values) {
                sum += val.get();
            }
            result.set(sum);
            context.write(key, result);
        }
    }

    public static void main(String[] args) throws Exception {
        Configuration conf = new Configuration();
        Job job = Job.getInstance(conf, "word count");
        job.setJarByClass(WordCount.class);
        job.setMapperClass(TokenizerMapper.class);
        job.setCombinerClass(IntSumReducer.class);
        job.setReducerClass(IntSumReducer.class);
        job.setOutputKeyClass(Text.class);
        job.setOutputValueClass(IntWritable.class);
        FileInputFormat.addInputPath(job, new Path(args[0]));
        FileOutputFormat.setOutputPath(job, new Path(args[1]));
        System.exit(job.waitForCompletion(true) ? 0 : 1);
    }
}
�˴�������Hadoop�ٷ��̳̣��������ο���

���������ļ�
WordCount�������ļ��ַ����м�������������Ľ����������Ҫ��������·����������WordCount�£�srcͬ��Ŀ¼���½�һ���ļ���input�������һ�������ı��ļ���input�У���Ϊʾ����

File List Input

���ﻹ��һ�����飬���File->Project Structure���ڵ������ĶԻ�����ѡ��Modules����Sourcesѡ�����Language level����Ϊ7����������õ��汾���ƵĻ������������ｫinput�ļ��б��ΪExcluded��

Screenshot Modules Settings

�������в���
����������Ҫ���ô˳�������ʱ��Main class���Լ�WordCount��Ҫ���������·����

��Intellij�˵�����ѡ��Run->Edit Configurations���ڵ������ĶԻ����е��+���½�һ��Application���á�����Main classΪWordCount�����Ե���ұߵ�...ѡ�񣩣�Program argumentsΪinput/ output/��������·��Ϊ�ղŴ�����input�ļ��У����Ϊoutput��

Screenshot Edit Configurations

���к͵���
����
����������ɺ󣬵���˵���Run->Run 'WordCount'����ʼ���д�MapReduce����Intellij�·�����ʾHadoop�����������������������Ϻ�Intellij���Ϸ�������µ��ļ���output�����е�part-r-00000�������еĽ���ˣ�

Screenshot Run

����Hadoop���趨���´�����ʱ���ɾ��output�ļ��У�

����
�ϵ����Ҳ�����ף�����Ҫ���õĴ���ǰ�������϶ϵ㣬����˵���Run->Debug 'WordCount'����ʼ���ԣ�������ڶϵ㴦ͣ�¡�

Screenshot Debug

Windows�µ�Ȩ������
Windows�����п��ܻ������ʾ

ERROR security.UserGroupInformation: PriviledgedActionException as ...
������Ϊ��ǰ�û�û��Ȩ��������·��Ȩ�ޣ�Linux�޴����⣩��һ����������Ǹ�hadoop�򲹶����ο�Failed to set permissions of path: tmp����Ϊ����ʹ�õ�Maven���˷�����̫�ʺϡ���һ�������ǽ���ǰ�û�����Ϊ��������Ա����������������������û����顱�����ã������Գ�������Ա��¼���д˳���

�����Ҿ�����õĽ����������Linux��macOS����hadoop��

С��
���������Ĳ�����Щ�࣬���߼��϶��Ǻ������ģ��й�һ�ξ����Ժ��֮������׶��ˣ���Ҫ������pom.xml�����ú����в����������ϡ�ɾ��WordCount��������в���Ҫ�κε�Hadoop����������������������ȫ������Maven����ˣ���ô�����ǲ��Ƿǳ��򵥣�

DEMO
��ʾ������������Github�ϣ��μ�zhantong/Hadoop-WordCount��