if_else
=======
//the correct format of if/else
lines = AsionIO.get_file_lines(AsionIO.logid_index() + '/logid_13_' + start_day + '.ig')
for line in lines:
    temp_line_list = line.strip().split('|')
    compare_day = ''.join(temp_line_list[0].split(' ')[0].split('-'))
    compare_day = datetime.datetime.strptime(compare_day, "%Y%m%d")
    if temp_line_list[1] in data_dic:
        if data_dic[temp_line_list[1]][4] == 0:
            data_dic[temp_line_list[1]][4] = "买道具"
            data_dic[temp_line_list[1]][6] = compare_day
        else:
            if compare_day < data_dic[temp_line_list[1]][6]:
                data_dic[temp_line_list[1]][4] = "买道具"
                data_dic[temp_line_list[1]][6] = compare_day
//中间变量的作用,否则出错
instead = (newcharger(day, hour)[1][newcharger(day, hour)[0][1]])[4]
ws.write(count_y, 5, instead.decode('utf8'))
