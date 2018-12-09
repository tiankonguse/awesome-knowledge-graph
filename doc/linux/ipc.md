# 共享内存


# 删除空内存

for key in $(ipcs|awk '{if ($6 == 0) print $1}'); do echo "delete $key"; ipcrm -M $key; done

