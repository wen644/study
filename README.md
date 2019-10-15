## study
# 命令行知识：
echo -n "要md5的字符串" | md5
打印中文
python回车
print u'\u****'
print '\x***'

## dSYM的使用 -见图片

## objc转成c语言
xcrun -sdk iphoneos clang -arch arm64 -rewrite-objc main.m
## 对象存储的地方
int age = 10;

int main(int argc, const char * argv[]) {
    @autoreleasepool {
        int a = 10;
        
        NSLog(@"数据段：age %p", &age);
        NSLog(@"栈：a %p", &a);
        NSLog(@"堆：obj %p", [[NSObject alloc] init]);
        NSLog(@"数据段：class %p", [MJPerson class]);
    }
    return 0;
}


## 取出对象的成员变量
//#import <objc/runtime.h>

//    unsigned int count;
//    Ivar *ivars = class_copyIvarList([UITextField class], &count);
//    for (int i = 0; i < count; i++) {
//        // 取出i位置的成员变量
//        Ivar ivar = ivars[i];
//        NSLog(@"%s %s", ivar_getName(ivar), ivar_getTypeEncoding(ivar));
//    }
//    free(ivars);
